<template>
    <div>
        <header>
            <div class="center">
                <div class="title">
                    <h3 class="top">safe environment with</h3>
                    <h1>Eco-Freak</h1>
                    <h3 class="bottom">world happy by your hand</h3>
                </div>
            </div>
            <div class="right">
                <label for="search-bar">
                    <img src="../assets/search-icon.png" class="icon" />
                    <input type="text" id="search-bar" name="search-bar" placeholder="Type to search...">
                </label>
            </div>
        </header>
        <section class="latest">
            <h3>Latest Post</h3>
            <div class="posts">
                <div class="post">
                    <div class="image" :style="{ backgroundImage: `url('${require('../assets/products.jpg')}')`}"></div>
                    <h4>Plan Ahead</h4>
                </div>
                <div class="post col-2 row-2">
                    <div class="image" :style="{ backgroundImage: `url('${require('../assets/products.jpg')}')`}"></div>
                    <h4>VueJS Fundamentals</h4>
                </div>
                <div class="post row-2">
                    <div class="image" :style="{ backgroundImage: `url('${require('../assets/products.jpg')}')`}"></div>
                    <h4>Alice Richardson</h4>
                </div>
                <div class="post row-2">
                    <div class="image" :style="{ backgroundImage: `url('${require('../assets/products.jpg')}')`}"></div>    
                    <h4>Parada Richardson</h4>
                </div>
                <div class="post">
                    <div class="image" :style="{ backgroundImage: `url('${require('../assets/products.jpg')}')`}"></div>
                    <h4>Learn Vue JS</h4>
                </div>
                <div class="post col-2">
                    <div class="image" :style="{ backgroundImage: `url('${require('../assets/products.jpg')}')`}"></div>
                    <h4>learn to take a break</h4>
                </div>
            </div>
            <div class="bottom">
                <button class="load">See More</button>
            </div>
        </section>
    </div>
</template>


<style lang="scss">
    header {
        display: flex;
        justify-content: center;
        padding: 50px 50px 25px;
        margin-left: 40em;

        .center {
            h3 {
                font-size: 20px;
                font-style: italic;
                font-weight: 400;
                margin: 0;

                &.bottom {
                    text-align: right;
                }
                &.top {
                    text-align: left;
                }
            }

            h1 {
                color: #171717;
                font-size: 72px;
                margin: 0;
            }

        }

        .right {
           flex: 1; 
           display: flex;
           justify-content: flex-end;

           label {
               position: relative;
               display: block;
               width: 300px;
               height: 35px;

               input {
                   width: 80%;
                   height: 35px;

                   background-color: #ffffff;
                   box-shadow: 2px 2px 8px 0px rgba(0, 0, 0, 0.2);

                   margin: 0;
                   padding: 5px 0px 0px 35px;
                   box-sizing: border-box;

                   appearance: none;
                   border: none;
                   outline: none;

                   color: #171717;
                   font-family: 'Rockwell', serif;
                   font-size: 14px;

                   &::placeholder {
                       color: #888888;
                   }
               }
               .icon{
                   position: absolute;
                   width: 25px;
                   margin: 5px;
               }
           }
        }

    }

    .latest {
        display: block;
        width: 100%;
        max-width: 1280px;
        margin: 0 auto;

        h3 {
            text-align: left;
        }
        .posts {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            grid-template-rows: repeat(3, 196px);
            grid-gap: 30px;

            margin: 15px;

                
            .post {
                display: flex;
                flex-direction: column;
                
                background-color: #ffffff;
                box-shadow: 3px 3px 8px 0px rgba(0, 0, 0, 0.2);


                .image {
                    flex: 1;
                    background-position: center;
                    background-size: cover;
                    background-repeat: no-repeat;
                }

                h4 {
                    font-size: 10px;
                    box-sizing: border-box;
                    padding: 3px 15px 0px 15px;
                    height: 50px;
                    line-height: 50px;
                    margin: 0px;
                }
                &.col-2 { 
                    grid-column: span 2;
                    flex: none;
                    max-width: none;
                }
                &.row-2 {
                    grid-row: span 2;
                }

            }
        }
    }
    .load {
        display: block;
        width: 100%;
        max-width: 180px;
        height: 40px;
        margin-left: 35em;
        outline: none;
        border: none;
        border-radius: 15px;
        appearance: none;

        background-color:  #42b983;
        box-shadow: 3px 3px 8px 0px rgba(0, 0, 0, 0.2);

        color: #171717;
    }
</style>
