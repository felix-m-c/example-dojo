# Welcome to JADE CTF 2!
*hover for more info*

a few facts about this platform:
- This definitely is the real jade 2
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
}

main div div:nth-child(2) {
  overflow-y: clip;
  max-height: 90px;
  transition: max-height linear .4s .5s;
  padding-inline: 1rem;
  padding-bottom: .4rem;
  border-radius: .2rem;
  &:hover {
    max-height: 2300px;
    background: #333;
    transition-delay: 0s;
  }
}

main div div:nth-child() {
  display: none;
}

h2.row:not(:nth-of-type(4)),
#stats-dashboard {
  display: none;
  &+br {
    display: none;
  }
}
```