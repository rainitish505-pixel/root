const menuToggle = document.querySelector(".menu-toggle");
const nav = document.querySelector(".nav");

if (menuToggle && nav) {
  menuToggle.addEventListener("click", () => {
    const isOpen = nav.classList.toggle("open");
    menuToggle.setAttribute("aria-expanded", isOpen);
    menuToggle.textContent = isOpen ? "✕" : "☰";
  });

  nav.querySelectorAll("a").forEach(link => {
    link.addEventListener("click", () => {
      nav.classList.remove("open");
      menuToggle.setAttribute("aria-expanded", "false");
      menuToggle.textContent = "☰";
    });
  });
}

const year = document.getElementById("year");
if (year) year.textContent = new Date().getFullYear();

const form = document.getElementById("enquiryForm");

if (form) {
  form.addEventListener("submit", function(event) {
    event.preventDefault();

    const data = new FormData(form);
    const message = `Hello Smart Tech Solutions!
Name: ${data.get("name")}
Phone: ${data.get("phone")}
Product: ${data.get("product")}
Message: ${data.get("message")}`;

    window.open(
      "https://wa.me/918010292729?text=" +
      encodeURIComponent(message),
      "_blank"
    );
  });
}
