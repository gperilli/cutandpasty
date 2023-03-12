## Javascript

Add event listener on iterated items
```
document.querySelectorAll("img").forEach((img) => {
  img.addEventListener("click", (event) => {
    event.currentTarget.classList.toggle("img-circle");
  });
});
```
