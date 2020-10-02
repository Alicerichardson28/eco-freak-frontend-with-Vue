<template>
    <div>
        <header>
            <div class="center">
                <div class="title">
                    <h3 class="top">helping the environment with</h3>
                    <h1>Eco-Freak</h1>
                    <h3 class="bottom">makes the world happy</h3>
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
            <h3>All Posts</h3>
            <div class="posts" v-if="posts.length >= 6">
                <div class="post">
                    <div class="image" :style="{ backgroundImage: `url('${require('../assets/ecoworld1.jpg')}')`}"></div>
                    <a href="http://ecoworld.org/10-small-ways-to-save-the-environment/">
                    <h4 :title="posts[0].title">{{ posts[0].title }}</h4>
                    </a>
                </div>
                <div class="post col-2 row-2">
                    <div class="image" :style="{ backgroundImage: `url('${require('../assets/ecoworld2.jpg')}')`}"></div>
                    <a href="http://ecoworld.org/planning-a-home-solar-electric-system/">
                    <h4 :title="posts[1].title">{{ posts[1].title }}</h4>
                    </a>
                </div>
                <div class="post row-2">
                    <div class="image" :style="{ backgroundImage: `url('${require('../assets/ecoworld4.jpg')}')`}"></div>
                    <a href="http://ecoworld.org/6-tips-to-tell-if-your-restaurant-is-eco-friendly/">
                    <h4 :title="posts[2].title">{{ posts[2].title }}</h4>
                    </a>
                </div>
                <div class="post row-2">
                    <div class="image" :style="{ backgroundImage: `url('${require('../assets/ecoworld3.jpg')}')`}"></div>    
                    <a href="http://ecoworld.org/tips-to-help-the-environment-and-save-money/">
                    <h4 :title="posts[3].title">{{ posts[3].title }}</h4>
                    </a>
                </div>
                <div class="post">
                    <div class="image" :style="{ backgroundImage: `url('${require('../assets/ecoworld5.jpg')}')`}"></div>
                    <a href="https://ecoworld.org/how-to-save-water-at-home/">
                    <h4 :title="posts[4].title">{{ posts[4].title }}</h4>
                    </a>
                </div>
                <div class="post col-2">
                    <div class="image" :style="{ backgroundImage: `url('${require('../assets/ecoworld6.jpg')}')`}"></div>
                    <a href="http://ecoworld.org/the-urban-techno-forest/">
                    <h4 :title="posts[5].title">{{ posts[5].title }}</h4>
                    </a>
                </div>
            </div>
            <div class="posts" v-else> 
                <p>Not enough posts to display</p>
            </div>
        </section>
            <Posts :posts="posts" :count="postCount" @showMore="this.showMore"/>
            <br><br><br><br>
            <NewBlog />
            <hr>
        <div class="footer-container">
          <h1 class="footer-app-name">Ecofreak</h1>
          <div class="footer-navbar">
            <router-link class="link" to="/">Home</router-link> 
            <router-link class="link" to="/about">About</router-link> 
            <router-link class="link" to="/product">Product</router-link> 
            <router-link class="link" to="/blog">Blog</router-link>
          </div>
        </div>
    </div>
    
</template>

<script>
import Posts from "./components/Posts"
import NewBlog from "./components/NewBlog"

export default {
    name: 'blog',
    components: {
        Posts,
        NewBlog
    },
    data () {
        return {
        API_URL:"/api/",
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
                this.posts = this.posts.sort(function (a,b) {
                    if (a.timestamp < b.timestamp) {
                        return -1
                    }
                    if (a.timestamp > b.timestamp) {
                        return 1
                    }
                    return 
                })
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

    .blog-form {
        width: 600px;
        display: flex;
        flex-direction: column;
        margin: 0 auto;
        margin-bottom: 5em;
    }

    .topic-form {
        text-align: left;
    }
    .lable-form {
        text-align: left;
    }
    textarea {
        height: 200px;
    }

    .footer-container {
    margin-top: 12px;
    height: 52px;
    margin-left: 10em;
    width: 90em;
    display: flex;
    align-content: flex-end;
    justify-content: space-between;
  }

  .footer-app-name{
    font-weight: 700;
    font-size: 150%;
    font-family: 'Josefin Sans', sans-serif;
    margin-bottom: 2em;
  }

  .footer-navbar {
    margin: 0;
    width:  100em;
    display: flex;
    justify-content: space-evenly;
    margin-bottom: 2em;

    font-weight: bold;
    color: #2c3e50;
    text-decoration: none;

  }

  a {
    color: #2c3e50;
  }
  a:hover, a:active, a:focus {
    color:#42b983;
  }
    
    
</style>
