<template>
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
                <input type="text" id="search-bar" name="search-bar" placeholder="Type to search..."">
            </label>
        </div>
    </header>
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
 
</style>
