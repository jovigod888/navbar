# navbar

## Estrutura do Projeto

projeto/
│├── index.html├── styles.css└── README.md

## Estrutura do HTML


## Estrutura do HTML

O arquivo `index.html` conterá a estrutura básica do HTML, incluindo a barra de navegação.

```html
<!DOCTYPE html>
<html lang="pt-br">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Hello world</title>
        <link rel="stylesheet" type="text/css" href="stylesheet.css" media="screen" />
    </head>
    <body>

        <style>
            @import url('https://fonts.googleapis.com/css2?family=Manrope');

body {
  background: rgb(2, 6, 23);
  height: 100svh;
  display: grid;
  place-items: center;
  
  font-family: "Manrope", sans-serif;
  color: white;
  font-size: clamp(1.5rem, 2vw + 1rem, 2.5rem);
  
  padding: 1rem;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body > svg {
  position: absolute;
  opacity: 0;
  height: 0;
  width: 0;
  pointer-events: none;
}

main {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 1fr auto;
  
  border: 3px solid #fff2;
  box-shadow: 0 8px 32px 0 #000;
  border-radius: 1em;
  overflow: hidden;
  
  max-width: 20rem;
  width: 100%;    
  > * {
    grid-column: 1;
  }
}

a {
  color: inherit;
  text-decoration: none;
}

.wrapper {
  height: 80vh;
  grid-row: 1/-1;
  flex: 1;
  overflow: hidden;
  position: relative;
}

iframe {
  width: 100%;
  height: 100%;
  height: 150%;
  z-index: 1;
}

img.preview {
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: -1;
  object-fit: cover;
}

nav {
  grid-row: 2;
  padding: 1.5rem;
  
  display: flex;
  justify-content: space-between;
  
  background: #0002;
  backdrop-filter: contrast(.9) blur(7px) url(#fluted);
  box-shadow: 0 8px 32px 0 #0008;
  
  > a {
    display: flex;
    align-items: center;
  }
  
  svg {
    width: 1.5rem;
    height: 1.5rem;
  }
}


a.highlight {
  background: #0002;
  padding: .25rem 1.5rem;
  border-radius: 1em;
  border: 3px solid #fff2;
  backdrop-filter: blur(10px);
}

        </style>

        <main>
            <div class="wrapper">
              <img class="preview" src="https://i.imgur.com/389Tx9h.png" alt=""/>
              <iframe src="https://cloudkid.com/all-releases" frameborder="0"></iframe>
            </div>
            <nav>
              <a href="#"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                  <use href="#tabler--archive" />
                </svg></a>
              <a href="#" class="highlight">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                  <use href="#tabler--search" />
                </svg>
              </a>
              <a href="#"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                  <use href="#tabler--send" />
                </svg></a>
            </nav>
          </main>
          
          <svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" color-interpolation-filters="sRGB">
            <!--
              ------
             🎹 Fluted
              ------
            -->
          
            <filter id="fluted" primitiveUnits="objectBoundingBox">
              <feImage x="0" y="0" in="blur_0" result="image_0" crossorigin="anonymous" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1 1' color-interpolation-filters='sRGB'>
                  <g>
                    <rect width='1' height='1' fill='black' />
                    <rect width='1' height='1' fill='url(%23red)' style='mix-blend-mode:screen' />
                    <rect width='1' height='1' fill='url(%23green)' style='mix-blend-mode:screen' />
                    <rect width='1' height='1' fill='url(%23yellow)' style='mix-blend-mode:screen' />
                  </g>
                  <defs>
                    <radialGradient id='yellow' cx='0' cy='0' r='1' >
                      <stop stop-color='yellow' />
                      <stop stop-color='yellow' offset='1' stop-opacity='0' />
                    </radialGradient>
                    <radialGradient id='green' cx='1' cy='0' r='1' >
                      <stop stop-color='green' />
                      <stop stop-color='green' offset='1' stop-opacity='0' />
                    </radialGradient>
                    <radialGradient id='red' cx='0' cy='1' r='1' >
                      <stop stop-color='red' />
                      <stop stop-color='red' offset='1' stop-opacity='0' />
                    </radialGradient>
                  </defs>
                </svg>" preserveAspectRatio="none meet" width=".03" height="1" />
              <feTile in="image_0" result="tile_0" />
              <feGaussianBlur stdDeviation=".003" edgeMode="none" in="tile_0" result="bar_smoothness" x="0" y="0" />
              <!--       <feGaussianBlur stdDeviation=".03" edgeMode="none" in="SourceGraphic" result="blur_glass" /> -->
              <feDisplacementMap scale=".08" xChannelSelector="R" yChannelSelector="G" in="SourceGraphic" in2="bar_smoothness" result="displacement_0" />
            </filter>
          
            <symbol id="tabler--send" viewBox="0 0 24 24">
              <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M10 14L21 3m0 0l-6.5 18a.55.55 0 0 1-1 0L10 14l-7-3.5a.55.55 0 0 1 0-1z" />
            </symbol>
          
            <symbol id="tabler--search" viewBox="0 0 24 24">
              <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M3 10a7 7 0 1 0 14 0a7 7 0 1 0-14 0m18 11l-6-6" />
            </symbol>
          
            <symbol id="tabler--archive" viewBox="0 0 24 24">
              <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M3 6a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2v0a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2m2 2v10a2 2 0 0 0 2 2h10a2 2 0 0 0 2-2V8m-9 4h4" />
            </symbol>
          </svg>    
    </body>
</html>

