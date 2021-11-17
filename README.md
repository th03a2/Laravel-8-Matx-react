# Laravel-8- with React free Template (Matx|Coreui)
Full stack Laravel 8 with Matx react.js<br>
Youtube: https://www.youtube.com/watch?v=HVVpbpNUJ8M<br>

<h2>Laravel 8 freshly install</h2>
Insatall to your local machine a feshly install laravel 8 or  You can follow the installation guidelines mentioned on the official Laravel documentation page, https://laravel.com/docs/7.x/installation.

coreui link: https://coreui.io/fd/?e=addtim52%40gmail.com&h=3898d3f1690d2bbf2bbc5331aa5d385c&utm_source=website&utm_medium=sendgrid&utm_campaign=website&affChecked=1&fbclid=IwAR06SP8RnNOjxgVn3xCRmC3VFlWMIXH106tkJPyMZcKjyvcL-CvHnncR1_Y

matx link: https://matx-react.ui-lib.com/dashboard/default

<h3>React Js<h3>
  Download a react template, then copy and paste on the laravel project resources title react.
  
<h2>Getting Started</h2>
<h2>Step 1: Set up Laravel into SPA</h2>
<h2>Update pages</h2>
 <pre>a. Update the resources/view/welcome.blade.php.</pre>
  <span>   check the source code.  </span>
 <pre>b. set the routes/web.php</pre>
   <pre>
       Route::get('/', function () {
          return view('welcome');
      });
    </pre>
   <pre>
       // to have single pages only.
        Route::get('/{any}', function () {return view('welcome');})->where('any', '.*');
        Auth::routes();
   </pre>
<h2>Then in the project root folder, you need to run the following commands. </h2>
  <small>Note: run only in git bash.</small>
<pre>composer require laravel/ui</pre>
<pre>php artisan ui react </pre>
 <pre>npm install laravel-mix@latest --save-dev</pre>
  <span>**If your Laravel version is lower than 7, you need to run “php artisan preset react”</span>

<pre>npm install && npm run dev</pre>
 
<h2>Step 2: Update Laravel dependencies</h2>
<pre> Go to package.json file</pre>
<pre>On your react Package.json, copy all dependencies and add to laravel Package.json dependencies to combine all react dependencies with laravel 8</pre>

<h2>Step 3: Update Laravel devDependencies</h2>
<pre>add '"react-scripts": "^3.4.3"'</pre>
<pre>On your both project, open the Package.json and update the devDependencies
      by combining all react devDependencies with laravel 8</pre>
   
 <h2>Step 5: create new page name ".babelrc"</h2>
  <pre>create .babelrc on the project</pre>
  <pre>{
    "presets": [
        "@babel/env",
        "@babel/preset-react"
    ],
    "plugins": [
        "@babel/plugin-syntax-dynamic-import",
        [
            "@babel/plugin-proposal-class-properties",
            {
                "loose": true
            }
        ]
    ]
}</pre>
 <h2>Step 6: update webpack.mix.js</h2>
  <pre>
  mix.js('resources/js/app.js', 'public/js')
    .react()
    .sass('resources/sass/app.scss', 'public/css');

mix.options({
    postCss: [require('autoprefixer')]
});
mix.setPublicPath('public');
mix.webpackConfig({
    resolve: {
        extensions: ['.js', '.vue'],
        alias: {
            '@': __dirname + 'resources'
        }
    },
    output: {
        chunkFilename: 'js/chunks/[name].js'
    }
})
mix.js('resources/react/src/index.jsx', 'public/js/app.js').version();
  </pre>
 <h2>Step 7: npm run development</h2>
 <h2>Step 8: npm run watch</h2>
 <h2>Step 9: php artisan serve</h2>
