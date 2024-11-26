<h1 align="left">Hey 👋 What's up?</h1>

###

<p align="left">My name is Bernardo and I am from Brazil!</p>

###

<h2 align="left">🎓 Software Engineering student at PUC-Minas, passionate about technology and programming.</h2>

###

<p align="left">💻 Exploring both front-end and back-end development | Continuously learning to create complete and efficient solutions.<br>💡 Interested in entering the tech industry, specializing, and continuously learning.<br>🌱 Continuously learning and enhancing my skills in Java, C, C++, JavaScript, HTML, CSS, and SQL.</p>

###

<h2 align="left">I code with</h2>

###

<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="40" alt="javascript logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="40" alt="html5 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="40" alt="css3 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" height="40" alt="c logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg" height="40" alt="cplusplus logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" height="40" alt="java logo"  />
</div>

###
name: Generate Snake

on:
  push:
    branches:
      - main
  workflow_dispatch:

jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - name: Clonar o repositório
        uses: actions/checkout@v2

      - name: Gerar a cobra
        uses: Platane/snk@v2
        with:
          github_user_name: <SEU_USUARIO>
          output: dist/github-contribution-grid-snake.svg

      - name: Fazer upload do SVG
        uses: actions/upload-artifact@v3
        with:
          name: snake-commit
          path: dist/github-contribution-grid-snake.svg
