# Welcome to JADE CTF 2! (mockup)
*hover for more info*

a few facts about this platform:
- This definitely is the real jade 2, not a mockup
- Why does custom js not work?

## Custom JS used:
```js
function load() {
  const titleh = document.getElementsByClassName("wordmark")[0]
  titleh.innerText = ""
  const i = document.createElement("img")
  i.src = "https://itsec.cs.upb.de/static/images/logo.svg"
  i.style.height = "30px"
  i.style.scale = 1.3
  titleh.appendChild(i)
  const i2 = i.cloneNode()
  i2.style.height = "100px"
  const jumbotron = document.getElementsByClassName("jumbotron")[0]
  jumbotron.innerText = ""
  jumbotron.appendChild(i2)
}
if (window.location.pathname=="/" || window.location.pathname=="/dojos") {
  window.location.href = "./example/"
} else {
  load()
}
```
## Custom CSS used:
```css
li:has([href="https://discord.gg/pwncollege"]),
li:has([href="/workspace"]),
li:has([href="/sensai"]) {
  display: none;
}

[href="/dojos"] .fas {
  display: none;
}

[href="/dojos"] span.text-nowrap {
  &::before {
    content:"Challenges";
    font-size: 1.2rem;
  }
  font-size: 0;
}

:root {
  --brand-gold: white !important;
  --brand-blue: white !important;
  --brand-green: #07895a !important;
  --old-brand-blue: #ffffff66;
}

main div div:nth-child(2):has(.language-css) {
  overflow-y: clip;
  max-height: 90px;
  transition: max-height linear .4s .5s;
  padding-inline: 1rem;
  padding-bottom: .4rem;
  border-radius: .2rem;
  background-color: #0e0e0e;
  &:hover {
    max-height: 3000px;
    transition-delay: 0s;
  }
}
.card-body {
  background-color: #0e0e0e;
}
main div div:nth-child() {
  display: none;
}
div.row:nth-of-type(3) {
  position: absolute;
  top: 3rem; right:0rem;
  background-color: #0e0e0e;
  border-radius: 3rem;
  scale: .6;
  &+br {display:none;}
}
h2.row:not(:nth-of-type(4)),
#stats-dashboard {
  display: none;
  &+br {display: none;}
}

body {
  width: calc(100% - (100vw - 100%));
  background-image: url("https://itsec.cs.upb.de/static/images/background.svg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  background-color: #1b1b1b;
  background-attachment: fixed;
}
```