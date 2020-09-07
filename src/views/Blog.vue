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
        <section class="latest" >
            <h3>Latest Post</h3>
            <div class="posts" v-if="posts.length >= 6">
                <div class="post">
                    <div class="image" :style="{ backgroundImage: `url('${require('../assets/ecoworld1.jpg')}')`}"></div>
                    <h4 :title="posts[1].title">{{ posts[1].title }}</h4>
                </div>
                <div class="post col-2 row-2">
                    <div class="image" :style="{ backgroundImage: `url('${require('../assets/ecoworld2.jpg')}')`}"></div>
                    <h4 :title="posts[2].title">{{ posts[2].title }}</h4>
                </div>
                <div class="post row-2">
                    <div class="image" :style="{ backgroundImage: `url('${require('../assets/ecoworld3.jpg')}')`}"></div>
                    <h4 :title="posts[3].title">{{ posts[3].title }}</h4>
                </div>
                <div class="post row-2">
                    <div class="image" :style="{ backgroundImage: `url('${require('../assets/ecoworld4.jpg')}')`}"></div>    
                    <h4 :title="posts[4].title">{{ posts[4].title }}</h4>
                </div>
                <div class="post">
                    <div class="image" :style="{ backgroundImage: `url('${require('../assets/ecoworld5.jpg')}')`}"></div>
                    <h4 :title="posts[5].title">{{ posts[5].title }}</h4>
                </div>
                <div class="post col-2">
                    <div class="image" :style="{ backgroundImage: `url('${require('../assets/ecoworld6.jpg')}')`}"></div>
                    <h4 :title="posts[6].title">{{ posts[6].title }}</h4>
                </div>
            </div>
            <div class="posts" v-else>
                <p>Not enough posts to display</p>
            </div>
        </section>
            <Posts :posts="posts" :count="postCount" @showMore="this.showMore"/>
    </div>
</template>

<script>
import Posts from "./components/Posts"

export default {
    name: 'blog',
    components: {
        Posts
    },
    data () {
        return {
        API_URL:"http://localhost:3000/api/",
        posts: [],
        postCount: 6
        }
    },
    methods: {
        getPosts () {
            fetch(this.API_URL + "posts/all")
            .then(data => {
                return data.json();
            })
            .then(json => {
                this.posts = json.result;
            })
        },
        showMore () {
            this.postCount += 2
        }
    },
    beforeMount() {
        this.getPosts();
    },
}
</script>


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
            margin-left: 13px;
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
                    overflow: hidden;

                    color: #171717;
                    font-size: 13px;
                    font-weight: 400;

                    text-overflow: ellipsis;
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
    
</style>
