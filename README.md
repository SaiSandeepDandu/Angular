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
Installation - 
1. Make sure node js is installed. [node -v]
2. Install angular CLI. [npm install -g @angular/cli]
   -g installs it globally.
3. ALl angular commands starts with 'ng'. To check version [ng --version]
4. Create angular application [ng new Appname]
5. Run Application [ng serve / npm start]
   [ng serve -o] : opens the application by default
   [ng serve -p XXXX] opens in a specific port that we give

Angular Component:
1. Its a combination of HTMS, CSS, .ts and test file.
2. 4 Major components of webpage: Header, Side nav, Body, Footer. Each having a separate component.
3. In .ts file, @component decorator is used and it converts a js file into a typescript file.
4. template url links html file to the component.
5. style url links the style sheets to the component. An array of paths to the various css files.