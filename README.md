# Initialization

1. initialize npm to add package

   ```
   npm init
   ```

2. install sass

   ```
   npm i node-sass
   ```

3. add "sass" to scripts

   ```
   "sass": "node-sass -w scss/ -o dist/css/ --recursive"
   ```

   -w: watch path of scss file

   -o: path of output css

4. run scss

   ```
   npm run sass
   ```
   
5. link css

​	

# Deployment

1. install gh pages

   ```
   npm i gh-pages
   ```

   

2. add homepage package

   ```
   "homepages": "https://jiaxinliu.github.io/modern_portfolio"
   ```

   

3. add deploy to scripts in package

   ```
   "deploy": "gh-pages -d dist"
   ```

4. npm run deploy



# Custom Domain

1. buy a domain name

   https://ap.www.namecheap.com/

2. domain list + manage

3. advanced DNS

   (1)	Type: a record, host: @, value: 185.199.108.153 ~ 185.199.111.153

   (2)	Type: CNAME, Host: www, value：185.199.108.153 

4. add custom domain in repo + setting + pages

# HTML

## Shortcuts

1. tag + . + class c1 + tab

   ```html
   <tag class = c1></tag>
   ```

2. .  + class c1 + tab

   ```html
   <div class = c1></div>
   ```

3. shift + alt + down => duplicatepr

   ```html
   <div class = c1></div>
   <div class = c1></div>
   <div class = c1></div>
   ```




## awesome fonts

1. link in head

   ```html
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.2.0/css/all.css" integrity="sha384-hWVjflwFxL6sNzntih27bfxkr27PmbbK/iSvJ+a4+0owXq79v+lsFkW54bOGbiDQ"
   ```

   

2. some icons

   ```html
   <i class="fab fa-twitter fa-2x"></i>
   <i class="fab fa-facebook fa-2x"></i>
   <i class="fab fa-linkedin fa-2x"></i>
   <i class="fab fa-github fa-2x"></i>
   ```

   



## Structure

1. header

   nav: unordered list + list item + a(href)

   ```html
   <header>
           <nav class="menu">
               <ul class="menu-nav">
                   <li class="nav-item">
                       <a href="index.html" class="nav-link">
                           Home
                       </a>
                   </li>
   
                   <li class="nav-item">
                       <a href="JIAXIN_s_Resume.pdf" class="nav-link">
                           Resume
                       </a>
                   </li>
   
                   <li class="nav-item">
                       <a href="projects.html" class="nav-link">
                           Projects
                       </a>
                   </li>
   
                   <li class="nav-item">
                       <a href="#" class="nav-link">
                           Contact
                       </a>
                   </li>
               </ul>
           </nav>
   </header>
   ```

   

2. main

   (1) overlay: div

   ```html
   <div class="overlay"></div>
   ```

   (2) multiple parts: div/h1/h2/... + p/a

   ```html
   <div class="intro">
               <h1 class="lg-heading">
                   Jiaxin 
                   <strong class="lastname">
                       Liu
                   </strong>
                   
               </h1>
   
               <p class="sm-heading">
                   I am a graduate CS student at Brown University.
                   My interest lies in data structure and algorithm, distributed system and  deep learning.
               </p>
           </div>
   
           <div class="icons">
               <a href="#">
                 <i class="fab fa-twitter fa-2x"></i>
               </a>
   
               <a href="#">
                 <i class="fab fa-facebook fa-2x"></i>
               </a>
   
               <a href="https://www.linkedin.com/in/jiaxin-liu-02180a219/">
                 <i class="fab fa-linkedin fa-2x"></i>
               </a>
               
               <a href="https://github.com/victorliu-sq">
                 <i class="fab fa-github fa-2x"></i>
                   					//size 2x
               </a>
   </div>
   ```

   

   

3. footer

   copyright

   ```html
   <footer>
   	Copyright &copy; 2022
   </footer>
   ```

   

# SCSS

## sort to specify

1. tag: body, main, header, footer, nav, h1, p, a
2. class of div



## when to use &

For example, if index.html, project.html and contact.html all have overlay but we want adjust opacity of index.html, we need to specify its id

```css
main{
    .overlay{
            
        }
    
    &#idofhtml{
        .overlay{
        	background: rgba($primary-color, 0.3);
        }
    }	
}
```



1. header(navbar)

   (1) overoall -> position fixed at top, background, width

   (2) li -> delete bullet, add right space, display inline(default block)

   (3) a -> color(default blue), delete underline

   ```css
   header{
       position: fixed;
       background: $primary-color;
       width: 100%;
   
       li{
           display: inline;
           list-style: none;
           padding-right: 15px;
           padding-bottom: 15px;
       }
       
   
       a{
           font-size: 1.2rem;
           text-decoration: none;
           color: white;
           &:hover{
               color: $secondary-color;
           }
       }
       
   }
   ```

   

2. body

   font style, line height

   ```css
   color:white;
   margin: 0; //if auto -->center
   font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
   line-height: 1.5;
   ```

   background image and overlay

   ```css
   background: $bg-img;
   background-attachment: fixed;
   background-size: cover;
   
   .overlay{
       z-index: -1;
       position: absolute;
       top:0;
       right: 0;
       width: 100%;
       height: 100%;
       background: rgba($primary-color, 0.8);
   }
   ```

   

3. main

   (1)  set footer to bottom of page

   ```
   min-height: calc(100vh - 30px);
   
   ```

   (2)  background, border, margin, pad

   ```
   background: rgba($secondary-color, 0.2);
   &:hover{
   	background: rgba($secondary-color, 0.5);
   }
   
   border-bottom: $secondary-color 3px solid;
   
   margin-top: 2rem;
   
   padding-top: 2rem;
   padding-bottom: 2rem;
   padding-left: 3rem;
   padding-right: 3rem;
   ```

   (3) font style and font pos

   ```css
   margin:auto;
   text-align: center;
   ```

   

4. footer

   ```css
   footer{
       text-align: center;
       font-size: 0.8rem;
       padding: 0.2rem 0.2rem;
   }
   ```

   

