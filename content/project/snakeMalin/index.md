---
title: SnakeMalin
summary: Self playing Snake game using A* algorithm to search food in the workspace by avoiding obstrucles.
tags:
  - ai
date: '2022-04-27'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: 
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: source
    url: https://github.com/SaadNeverSad/snakeMalin
url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.

---
This is a self playing Snake game using A* algorithm , watch the video below and enjoy the computer playing itself

{{< youtube taVOEMFuwUA >}}

To make the snake autonomous, we use the A* algorithm, the principle is to use a heuristic value (Manhattan distance between our head and the food), thus, our algorithm does not only take into account the arrival point, but also the set of possibilities already searched, using the distance between the departure and arrival points as a heuristic. We thus compute the set of possible paths and return the best (shortest) one. 
To increase the difficulty, we have added the presence of walls, which are randomly generated at the beginning of the game, and which are intended to prevent our snake to make only diagonals or straight lines to reach the food, as it could do if there were no wall.







