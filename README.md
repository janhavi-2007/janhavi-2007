<!-- ===================== ANIMATED HEADER ===================== -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:2563EB,100:06B6D4&height=200&section=header&text=Janhavi%20Suryawanshi&fontSize=42&fontColor=ffffff&animation=fadeIn" />
</p>

<!-- ===================== TYPING SVG ===================== -->
<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=24&pause=1200&color=58A6FF&center=true&vCenter=true&width=700&lines=Hi+👋+I'm+Janhavi;BTech+IT+Student;Cloud+%26+DevOps+Enthusiast;Java+|+C+|+C%2B%2B+|+Python;Learning+%26+Building+Daily+🚀" />
</p>

<!-- ===================== VISITOR COUNTER ===================== -->
<p align="center">
  <img src="https://komarev.com/ghpvc/?username=janhavi-2007&label=Profile%20Views&color=2563eb&style=for-the-badge" />
</p>

<!-- ===================== BADGES ===================== -->
<p align="center">
  <img src="https://img.shields.io/badge/Primary-Java-2563EB?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Core-C%20%7C%20C++-06B6D4?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Scripting-Python-22D3EE?style=for-the-badge" />
</p>

<!-- ===================== ABOUT ME ===================== -->
<h2 align="center" style="color:#58A6FF;">🚀 About Me</h2>

<p align="center">
🎓 BTech IT Student <br>
☁️ Cloud & DevOps enthusiast <br>
💻 Strong foundation in Java, C, C++ & Python <br>
⚙️ Interested in Automation, CI/CD & System Design
</p>

<!-- ===================== TOP LANGUAGES (CUSTOM) ===================== -->
<h2 align="center" style="color:#58A6FF;">💻 Programming Languages</h2>

<p align="center">
  <img src="https://skillicons.dev/icons?i=java,c,cpp,python&theme=dark" />
</p>

<!-- ===================== CONTRIBUTION SNAKE ===================== -->
<h2 align="center" style="color:#58A6FF;">🐍 Contribution Graph</h2>

<p align="center">
  <img src="https://raw.githubusercontent.com/janhavi-2007/janhavi-2007/output/github-contribution-grid-snake.svg" />
</p>

<!-- ===================== CONNECT ===================== -->
<h2 align="center" style="color:#58A6FF;">🤝 Connect With Me</h2>

<p align="center">
  <a href="https://www.linkedin.com">
    <img src="https://img.shields.io/badge/LinkedIn-2563EB?style=for-the-badge&logo=linkedin&logoColor=white"/>
  </a>
  <a href="mailto:yourmail@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-06B6D4?style=for-the-badge&logo=gmail&logoColor=white"/>
  </a>
</p>

<!-- ===================== FOOTER ===================== -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:06B6D4,100:2563EB&height=120&section=footer"/>
</p>
name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: janhavi-2007
          outputs: |
            dist/github-contribution-grid-snake.svg
      - uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
