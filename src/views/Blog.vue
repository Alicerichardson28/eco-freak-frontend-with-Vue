<template>
    <header>
        <div class="right">
            <label for="search-bar">
                <img src="../assets/search-icon.png" class="icon" />
                <input type="text" id="search-bar" name="search-bar" placeholder="Type to search..."">
            </label>
        </div>
    </header>
    <!-- <div class="jumbotron text-center hoverable p-4">
    <div class="row">
        <div class="col-md-4 offset-md-1 mx-3 my-3">

        <div class="view overlay">
            <img src="../assets/eco-friendly.jpg" class="img-fluid" >
            <a>
            <div class="mask rgba-white-slight"></div>
            </a>
        </div>

        </div>

        <div class="col-md-7 text-md-left ml-3 mt-3">

        <a href="#!" class="green-text">
            <h6 class="h6 pb-1"><i class="fas fa-desktop pr-1"></i> Nature</h6>
        </a>

        <h4 class="h4 mb-4">7 Eco Friendly Bloggers we LOVE!</h4>

        <p class="font-weight-normal">If you're interested in living a more eco-friendly life, we've rounded up 10 blogs that you should be reading! 
        These blogs are encouraging, helpful, and truly break eco-friendly living down in a friendly and approachable way. </p>
        <p class="font-weight-normal">by <a><strong>pelacase.com</strong></a>, 07/08/2018</p>

        <a class="btn btn-success" href="https://pelacase.com/blogs/news/7-eco-friendly-bloggers-we-love?gclid=CjwKCAjwkJj6BRA-EiwA0ZVPVoxFGgE9SKGr_oJsNz5Cwej5d2zqa9FHj19RWfaTqTpKtzjA7Pev4BoCrQcQAvD_BwE">Read more</a>
        </div>
    </div>
    <br><br><br><br><br>
    <div class="row">

        <div class="col-md-4 offset-md-1 mx-3 my-3">

        <div class="view overlay">
            <img src="../assets/products.jpg" class="img-fluid" >
            <a>
            <div class="mask rgba-white-slight"></div>
            </a>
        </div>

        </div>

        <div class="col-md-7 text-md-left ml-3 mt-3">
x
        <a href="#!" class="green-text">
            <h6 class="h6 pb-1"><i class="fas fa-desktop pr-1"></i> Nature</h6>
        </a>

        <h4 class="h4 mb-4">What are the Benefits of Compostable Packaging?</h4>

        <p class="font-weight-normal">THE BENEFITS OF COMPOSTABLE PACKAGING AND DISPOSABLES
        You’ve probably heard the term ‘compostable food packaging’, but do you know what it is and how using it could benefit your business? </p>
        <p class="font-weight-normal">by <a><strong>Nisbets Plc. Catering Equipment Supplies</strong></a>, 07/08/2018</p>

        <a class="btn btn-success" href="https://www.nisbets.co.uk/what-benefits-compostable-packaging-disposables">Read more</a>
        </div>
    </div>
    </div> -->
</template>

<style lang="scss">
    header {
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
