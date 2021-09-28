Steve talks about the web performance in the session.

 100ms is a gold standard for loading UI+Data.
 If your UI takes 10 sec or more to respond to an interaction, then we should talk.
 
 1 sec slow down resulted 11 % fewer page views, 7% less conversion.
 
 53% users will leave the mobile site if it takes more than 3 sec.
 
 
 Three different kinds of performance:
 
 1) Network load performance
 2) Javascript performance
 3) Rendering Performance
 
 While developing an application, we should think about only those parts first, which are important for the user, Rest of the components can be lazy loaded.
 Set Performance budget as well for the application.
 
 
  Doing Less stuff, will take less time.
  
  
 1) Network load performance: Until the user actually gets the page, there isn't much to optimize.
 2) Javascript performance: 
     Write code that runs faster.
 3) Rendering Performance: 
   Our javascript happens in the browser, which has tis own performance.
 
 
 Javascript Performance:
    Javascript which we are sending to UI to run, it increasing day by day.
    
    
 JIT:
 
 It means that there is compilation step. compilation happens a moment before real execution. compilation happens on the client machine's browser.  
 Chrome- v8
 Safari = Javascript Core
 Mozilla- Spider monkey
 
 
 Parsing happens in two phases:
 
 Eager: parses everything.
 Lazy: it does the bare minimum.
 
 how to eager parse a function: 
 (function add(a,b){return a+b;})
 
 
 Webpack plugin:
   optimize-js-plugin
 
NOTE: 
  try to avoid nested functions.
   

Optimizing Compiler: 
  
  TurboFAN+V8
  
  Speculative optimization
  Hidden classes for dynamic lookups.
  Function inlining.

node --trace-turbo-inlining

Points to remember when writing javascript code.
1) Initialize your properties at creation.
2) Initializa them in the same order.
3) Try not to modify them after the fact.
4) Maybe just use Typescript or Flow so you dont have to worry about these things.

 
 
 
 
 Build tools:
  purifycss - removes the css which we are not using.
  Babel: It allows us to write the future javascript and transpile it, into javascript that works in both old or modern browsers.
  Useful babel plugins:
     babel-presets-env
     @babel/plugin-transform-react-inline-elements
     
     
  
  
  
 
 
 
 
