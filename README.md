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

   

# SCSS

## set primary color of background and font

