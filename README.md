<!-- ===================== ANIMATED HEADER ===================== -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:2563EB,100:06B6D4&height=200&section=header&text=Welcome%20to%20My%20GitHub&fontSize=40&fontColor=ffffff&animation=fadeIn" />
</p>

<!-- ===================== TYPING SVG ===================== -->
<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=24&pause=1000&color=58A6FF&center=true&vCenter=true&width=650&lines=Hi+👋+I'm+Janhavi;BTech+IT+Student;Future+Cloud+%26+DevOps+Engineer;Learning+Every+Day+🚀" />
</p>

<!-- ===================== VISITOR COUNTER ===================== -->
<p align="center">
  <img src="https://komarev.com/ghpvc/?username=janhavi-2007&label=Profile%20Views&color=2563eb&style=for-the-badge" />
</p>

<!-- ===================== BADGES ===================== -->
<p align="center">
  <img src="https://img.shields.io/badge/Focus-Cloud%20%26%20DevOps-2563EB?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Languages-C%20|%20C++%20|%20Python-06B6D4?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Learning-AWS%20|%20Docker%20|%20Linux-22D3EE?style=for-the-badge" />
</p>

<!-- ===================== ABOUT ME ===================== -->
<h2 align="center" style="color:#58A6FF;">🚀 About Me</h2>

<p align="center">
🎓 BTech IT Student <br>
☁️ Passionate about Cloud & DevOps <br>
⚙️ Interested in Automation & Scalable Systems <br>
📈 Growing every day with consistency
</p>

<!-- ===================== GITHUB STATS ===================== -->
<h2 align="center" style="color:#58A6FF;">📊 GitHub Stats</h2>

<p align="center">
  <img width="48%" src="https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=github_dark&hide_border=true" />
  <img width="48%" src="https://github-readme-streak-stats.herokuapp.com/?user=YOUR_USERNAME&theme=github-dark&hide_border=true" />
</p>

<!-- ===================== TOP LANGUAGES ===================== -->
<p align="center">
  <img width="45%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_USERNAME&layout=compact&theme=github_dark&hide_border=true" />
</p>

<!-- ===================== CONTRIBUTION SNAKE ===================== -->
<h2 align="center" style="color:#58A6FF;">🐍 Contribution Graph</h2>

<p align="center">
  <img src="https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_USERNAME/output/github-contribution-grid-snake.svg" />
</p>

<!-- ===================== CONNECT ===================== -->
<h2 align="center" style="color:#58A6FF;">🤝 Connect With Me</h2>

<p align="center">
  <a href="https://www.linkedin.com/">
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
    - cron: "0 0 * * *"   # every day
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - uses: Platane/snk@v3
        with:
          github_user_name: YOUR_USERNAME
          outputs: |
            dist/github-contribution-grid-snake.svg

      - name: Push snake
        uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

