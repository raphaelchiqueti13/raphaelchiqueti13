# Olá, eu sou o Raphael Chiqueti! 👋

Estudante de **Ciência da Computação** na **UNICID** (2º semestre) e entusiasta do desenvolvimento **Front-end**. Gosto de transformar ideias em interfaces interativas e funcionais.

### 💻 Minha Stack de Estudos:
- **Linguagens:** HTML5, CSS3 e JavaScript (ES6+).
- **Frameworks/Libraries:** React.js.
- **Ferramentas:** Git, GitHub e VS Code.

### 🚀 Sobre mim:
- 🎓 Atualmente aprofundando meus conhecimentos em lógica de programação e arquitetura de sistemas na faculdade.
- 🎨 Focado em criar experiências de usuário (UX) modernas e responsivas com React.
- 💼 Tenho facilidade com resolução de problemas e comunicação, habilidades que trouxe das minhas experiências anteriores em logística e atendimento.



<div style="display: inline_block"><br>
  <img align="center" alt="Rapha-Js" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-plain.svg">
  <img align="center" alt="Rapha-Ts" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-plain.svg">
  <img align="center" alt="Rapha-React" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg">
  <img align="center" alt="Rapha-HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
  <img align="center" alt="Rapha-CSS" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
  <img align="center" alt="Rapha-Python" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
  <img align="center" alt="Rapha-Csharp" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/csharp/csharp-original.svg">
</div>
  
<a href="https://www.linkedin.com/in/raphael-chiqueti-bezerra-36ba3a252" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>
 <a href = "raphaelchiqueti@hotmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
  
name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: rafaballerini
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
