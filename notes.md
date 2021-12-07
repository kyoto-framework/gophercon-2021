
# Slide 1

Hello everyone!  
Today I'd like to present the library named kyoto.  

# Slide 2

But first, let me introduce myself.  
I'm Yurii Zinets.  
Software Engineer at Akamai, but also a Core Developer of BrokerOne Real Estate platform on part time.  
Overall story I'm going to tell is actually related to BrokerOne development process.

# Slide 3

A long story short.  
In the begining of the platform creation we decided to create a prototype first.  
We took well-known JS framework with set of ready for use material components.  
As usually happens, the prototype becomes the main project.  
Over the time, we began to feel the impact of this decision.  
It was hard to keep the project clean and tidy. We had a lot of problems with SSR, memory leaks on the server side and performance score issues.  
We completely lost control. After discussion, our team decided to drop this prototype and go in more traditional way - use template engine.

# Slide 4

So, why did we choose such a radical way?  
We had several reasons. Unnecessary complexity was one of those reasons.  
Not many people really understand how their project setup really works under the hood.  
Webpack with tons of configurations, babel, tree shaking (espesially when it doesn't work as expected), lazy loading.  
You need to bring a significant runtime and Virtual DOM just to render a simple things like articles or pages with minimal dynamic behavior.  
Template engine reduces overall complexity and allows to take full control over frontend.  
Also, this approach reduces amount of bugs and quirks, we can find most of the problems on building and testing stage.  

# Slide 5

Our project became much better with this migration, but we faced some common inconveniences.  
We have started to use more copy-paste.  
Our handlers became a spaghetti because of asynchronous DTO requests.  
And we all have to admit, vanilla JS is quite verbose even for simple dynamic things.  
That's how kyoto was born.

# Slide 6

Not ready yet

# Slide 7

Not ready yet

# Slide 8

Not ready yet
