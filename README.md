1. # EVENTLOOP
Because Javascript is singlethreaded, it means it executes tasks in a FIFO basis. Tasks that are not done are sent to an Event queue, waiting to be completed. A Loop checks this Queue to make sure it keeps churning out tasks until all are done. This Loop is called the Event Loop
2. # Explain the 6 phases of the event loop 
1. Timers phase: We have the setTimers phase(setInterval and setTimeOut)- these are kept in a heap memory until they are expired. If these timers get expired then the event loop takes this expired timers and starts executing them. Any timers set to 0 ms and setImmediate() run here
2. Pending Callbacks: The loop executes any system related callbacks if any
3. Idle/Prepare: In this phase the event loop does nothing. It is idle and prepares to go to the next phase
4. Poll Phase: It watches out for I/O callbacks.  Nearly all the callbacks except the setTimeout, setInterval, setImmediate and closing callbacks are executed.
5. Check/setImmediate: executes any setImmediate timers added to the poll phase. 
6. Closing: it executes callbacks associated with closing events like socket.on(process.exit)

3. #  List some best practices in server-side code development 
1. Focus on Code Quality: Use prettier for formatting and to check syntax consistency. ESlint is also used to check for patterns to ensure you deifne functions before calling them. 
2. Prefer AS6 and Async/await: in other for code to be more readable, the Async/Await syntax is the easiset to read 
3. Keep code small- node.js is built for scalability. You can group similar functions into modules using the npm. 
4. Error Handling: users making requests and developers need to know about errors. User should be presented with feedback of what happened while the developer should be writing and presenting relevant error messages to locate edge cases 
4. # What is NPM
Node package Manager is used for managing project dependencies via command line. Modules are shared as packages and packages extend the functionality of your app. 

5. # How do you initialize a package in npm 
npm init

5. # How do you run a script in the package.json ? 
npm run <name of script>
6. # Initialize a package of your choice, give it a name and install the following npm packages to it, express, mongoose, joi
Refer to package.json