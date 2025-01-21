# 📋 Résumé + CV + Coverletter

A repository containing the LaTeX source of Spencer Imbleau's résumé, curriculum vitae, and coverletter matter. Tested and deployed with GitHub Actions.

---
[![résumé last release](https://img.shields.io/github/release-date/simbleau/resume?logo=github&label=Last%20Release)](https://github.com/simbleau/resume/releases)
[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/simbleau/resume/ci.yml?logo=github&label=CI)](https://github.com/simbleau/resume/actions/workflows/ci.yml)

## 🤖 Deployment

Deployment is automated by [GitHub Actions](https://github.com/simbleau/resume/actions).

- Pushes to `main` trigger a new release of the [latest résumé, cv, and cover letter](https://github.com/simbleau/resume/releases/tag/latest), available in several formats.

  | Artifact               | Link                                                                          | Mirror                                         |
  | ---------------------- | ----------------------------------------------------------------------------- | ---------------------------------------------- |
  | Résumé                 | <https://simbleau.github.io/resume/resume.html>                               | <https://simbleau.github.io/resume/>           |
  | Résumé, Embedded       | <https://simbleau.github.io/resume/resume-embed.html>                         | <https://simbleau.github.io/resume/embed.html> |
  | Résumé, Download       | <https://github.com/simbleau/resume/releases/download/latest/resume.pdf>      |                                                |
  | CV                     | <https://simbleau.github.io/resume/cv.html>                                   |                                                |
  | CV, Embedded           | <https://simbleau.github.io/resume/cv-embed.html>                             |                                                |
  | CV, Download           | <https://github.com/simbleau/resume/releases/download/latest/cv.pdf>          |                                                |
  | Cover letter           | <https://simbleau.github.io/resume/coverletter.html>                          |                                                |
  | Cover letter, Embedded | <https://simbleau.github.io/resume/coverletter-embed.html>                    |                                                |
  | Cover letter, Download | <https://github.com/simbleau/resume/releases/download/latest/coverletter.pdf> |                                                |
- Manually pushed [releases](https://github.com/simbleau/resume/releases) also trigger workflows to upload artifacts.

## 🔧 Building

### Dependencies

- [TeXLive, full](https://www.tug.org/texlive/)
- [Make](https://www.gnu.org/software/make/)
- [j2cli](https://github.com/kolypto/j2cli)

### Commands

- **Build the résumé**:

  ```bash
  make resume
  ```

- **Build the cirriculum vitae**:

  ```bash
  make cv
  ```

- **Build the cover letter**:

  ```bash
  make coverletter
  ```

- **Build all**:

  ```bash
  make all
  ```

- **Purge all**:

  ```bash
  make clean
  ```

- **Open PDFs**:

  ```bash
  make open
  ```

## Creating icons

- Most icons come from the [`fontawesome5`](https://ctan.org/pkg/fontawesome5?lang=en) TeX package \[[with documentation](http://mirrors.ctan.org/fonts/fontawesome5/doc/fontawesome5.pdf)\].
- Some are custom made (those not in `fontawesome5`).
  - Find an open-licensed SVG vector on <https://www.svgrepo.com>
  - Ensure whitespace is cropped from the SVG `viewBox`: <https://svgcrop.com/>
  - Minify and strip the resulting SVG: <https://jakearchibald.github.io/svgomg/>
  - Convert svg to png: `inkscape --export-type png -w 1024 --export-filename /path/to/new.png /path/to/my.svg`

## 🔏 License

This project is [MIT](./LICENSE) licensed. You are within your rights to fork my résumé and use it as your own, although you should probably change my name to yours!
