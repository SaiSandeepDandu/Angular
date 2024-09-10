# Angular notes
Roadmap:
1. Project Structure
2. Components
3. Data Binding
4. Component communication
5. Directives
6. Routing
7. Forms: Template driven and Reactive
8. Pipes: Convert the input from one format to other
9. Services
10. HTTP

Angular CLI: Works on commands
### Installation - 
1. Make sure node js is installed. [node -v]
2. Install angular CLI. [npm install -g @angular/cli]
   -g installs it globally.
3. ALl angular commands starts with 'ng'. To check version [ng --version]
4. Create angular application [ng new Appname]
5. Run Application [ng serve / npm start]
   [ng serve -o] : opens the application by default
   [ng serve -p XXXX] opens in a specific port that we give

Angular Component and Project Structure:
1. Its a combination of HTMS, CSS, .ts and test file.
2. 4 Major components of webpage: Header, Side nav, Body, Footer. Each having a separate component.
3. In .ts file, @component decorator is used and it converts a js file into a typescript file.
4. template url links html file to the component.
5. style url links the style sheets to the component. An array of paths to the various css files.
6. In style sheets, three ways of defining the styles:
   a) tag {}  - to directly apply the style to the tag
   b) .class  - to define style to the class
   c) #id  - to define style to the id

7. Component selector tag is given in the body tag of index.html file.
8. Every angular app needs atleast one module and one component. Assets file has application related files like images etc. Can access these files using the path of assets file in the html file.
9. An application can be divided into multiple modules like login, registration and product module. Related components can be grouped into single module. Ex: Products module has different components like dresses, mobiles etc.
9. Environment.ts file has all env conditions for dev. env.prod.ts has prod specific environment conditions.
10. 'favicon' file has the application icon.
11. 'index.html' is the file that loads in the browser.
12. 'main.ts' file specifies which module to run first. We bootstrap the module that should first run.
13. 'style.css' file can be used to apply styles for all components of the application.
14. 'Browserrc' is used to specify browser related information.
15. 'editorconfig' file to specify editor related information.
16. 'gitignore' is used to specify the files that are to be ignored/not uploaded on git.
17. When the application is downloaded from git use [npm install] cmd to install all node modules/dependencies that are present in the package.json file.
18. 'angular.json' file specifies different app related configurations like index, main, styles, assets   etc. 


Data Binding:
1. It enables or facilitates the communication between html file and ts file. Either to display the data from .ts file on .html file or to access the data taken from .html file on the .ts file.
2. Data binding classifies into two types:
   a) One way Data Binding: two ways:
   1. Model/.ts  --> DOM/html
   2. DOM/html  --> Model/.ts
   b) Two way Data Binding:
      Model/.ts  <--> DOM/html

3. One Way Data Binding: There are few types of One way Data Binding, They are:
   Note: a,b,c,d are methods used to pass data from .ts to HTML file.
   a) String interpolation
   b) Attribute binding
   c) Class Binding
   d) Style Binding
   e) Event Binding

a) String Interpolation: To pass data from typescript(.ts) file to HTML file using {{}}. Can pass variables, expressions and function in {{}}.
   Ex: title = 'Demo';
       HTML: <h1>{{title}}</h1>
b) Property Binding: Property is nothing but an attribute of a html tag. Property binding involves binding/assigning the data from .ts file to the html property in the .html file. 
   Ex: ``` <img src={{path}}>
       In above tag, path is defined in the .ts file.
c) Class Binding: 

d) Style Bindng: To bind styles to the html elements from the .ts file. Just define the style in the .ts file and assign them directly in the html tags.
   Ex 1: .ts: cvar:string = 'blue';
       HTML: <h1 [style.color]="cvar">Hello</h1>
Can Also declare multiple styles using object.
   Ex 2: .ts: mystyle:object = {
      color: 'blue',
      background: 'grey'
   }
      HTML: <h1 [style]="mystyle">Hello</h1>
Also bind the styles based on the condition
   Ex 3: .ts: hasError:boolean = true;
         HTML: <h1 [style.color]="hasError?'red':'green'">Hello</h1>

e) Event Binding: Its also a one way data binding. Transfer data from html to .ts. Ex: Click, Double click, Hover.
   There are various types of events like mouse events, keyboard, focus, form(submit, reset, change) events
   Syntax: (eventname) = somefunc()
            on-eventname = somefunc()
   Ex: HTML: <button (click)="withdraw()">increment</button>
      
       .ts: counter:number = 0;
       increment(){
         this.counter += 1;
       }










