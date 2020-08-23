<template>
    <div>
        <div class="first-container">
            <img class="img-card" src="../assets/turtle1.png">
        </div> 
        <div class="second-container"> 
        </div> 
        <div>
            <h1 class="first-content">Eco-Friendly Products That'll Get <br> You A Little Closer To Saving The Planet</h1>
        </div>
        <div class="cards-container">
            <ul class="cards-ul">
                <li class="card">Compostable Plates</li>
                <li class="card">Tree-Free Dinner Napkin</li>
                <li class="card">Compostable Bowls</li>
                <li class="card">Hot Cups</li>
                <li class="card">Compostable Takeout Containers</li>
                <li class="card">Compostable Tablecloth</li>
                <li class="card">Compostable Cutleries</li>
                <li class="card">Compostable PLA Cold Cups</li>
                <li class="card">Compostable Trash Bag</li>
                <li class="card">reusable straws</li>
                <li class="card">paper straws//Pasta straws</li>
                <li class="card">Tree - Free Bath Tissue</li>
            </ul>
        </div>
    </div> 

</template>

<style lang="scss">
    @import url('https://fonts.googleapis.com/css2?family=Gothic+A1:wght@200;300;400&family=Josefin+Sans:ital,wght@0,200;1,500;1,700&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Gothic+A1:wght@200;300;400&family=Josefin+Sans:ital,wght@0,200;0,400;1,500&display=swap');
    html, body, div, span, applet, object, iframe,
    h1, h2, h3, h4, h5, h6, p, blockquote, pre,
    a, abbr, acronym, address, big, cite, code,
    del, dfn, em, img, ins, kbd, q, s, samp,
    small, strike, strong, sub, sup, tt, var,
    b, u, i, center,
    dl, dt, dd, ol, ul, li,
    fieldset, form, label, legend,
    table, caption, tbody, tfoot, thead, tr, th, td,
    article, aside, canvas, details, embed, 
    figure, figcaption, footer, header, hgroup, 
    menu, nav, output, ruby, section, summary,
    time, mark, audio, video {
        margin: 0;
        padding: 0;
        border: 0;
        font-size: 100%;
        font: inherit;
        vertical-align: baseline;
    }
    /* HTML5 display-role reset for older browsers */
    article, aside, details, figcaption, figure, 
    footer, header, hgroup, menu, nav, section {
        display: block;
    }
    body {
        line-height: 1;
    }
    ol, ul {
        list-style: none;
    }
    blockquote, q {
        quotes: none;
    }
    blockquote:before, blockquote:after,
    q:before, q:after {
        content: '';
        content: none;
    }
    table {
        border-collapse: collapse;
        border-spacing: 0;
    }
    strong {
        font-weight: bold;
    }

    hr {
        margin: 0;
    }
    .first-container {
        width: 100%;
        height: 300px;
        background-color: #48996a;
    }
     .second-container {
        width: 100%;
        height: 300px;
        background-color: #71a6a7;
    }
    .img-card {
        margin-top: 10em;
        margin-right: 35em;
        width: 25%;
        -webkit-filter: drop-shadow(5px 5px 5px #222 );
        filter: drop-shadow(5px 5px 5px #222);
    }
    .first-content {
        margin: 2em;
        font-size: 150%;
        font-weight: 700;
        font-family: 'Josefin Sans', sans-serif;
        color: black;
    }

    .cards-container {
        width: 100%;
    }
    .cards-ul {
        width: 100%;
        display: grid;
        grid-template-columns: repeat(4, auto);
        grid-gap: 10px;
    }
    .card {
        width: 200px;
        height: 300px;
        justify-content: flex-end;
        margin: 0 auto;
    }
</style>

