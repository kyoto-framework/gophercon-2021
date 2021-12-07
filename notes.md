
# Slide 1

Hello everyone!  
Today I'd like to present the library named kyoto.  
It's an SSR-first go frontend library.  
And if it's not so interesting for you, feel free to take a cup of coffee during this 7 minutes :)  

# Slide 2

First, let me introduce myself.  
I'm Yurii Zinets.  
Software Engineer at Akamai, but also a Core Developer of BrokerOne Real Estate platform on part time.  
Overall story I'm going to tell is actually related to BrokerOne development process.  

# Slide 3

Before I start to talk about kyoto itself, it's important to know backstory because we are not creating technologies for technologies, but for solving different problems.  
So, a long story short.  
In the beginning of the platform creation we decided to create a prototype first.  
We took well-known JavaScript framework with set of ready for use material components.  
As usually happens, the prototype became the main project.  
Over the time, we began to feel the impact of this decision.  
It was hard to keep the project clean and tidy. We had a lot of problems with SSR, memory leaks on the server side and performance score issues.  
We completely lost control. After discussion, our team decided to drop this prototype and go in more traditional way - use template engine.

# Slide 4

So, why did we choose such a radical way?  
We had several reasons.  
Unnecessary complexity was one of those reasons.  
Not many people really understand how their project setup works under the hood.  
Webpack with tons of configurations, babel, tree shaking (espesially when it doesn't work as expected), lazy loading.  
You need to bring a significant runtime and Virtual DOM just to render a simple things like articles or pages with minimal dynamic behavior.  
Template engine reduces overall complexity and allows to take full control over frontend.  
Also, this approach reduces amount of bugs and quirks because we can find most of the problems on building and testing stages.  

# Slide 5

Our project became much better with this migration, but we faced some common inconveniences.  
We have started to use more copy-paste.  
Our handlers became a spaghetti because of asynchronous API and DB requests.  
And we all have to admit, vanilla JS is quite verbose even for simple dynamic things.  
That's why kyoto was born.

# Slide 6

So, how it solves these issues?  
First issue I solved is code organization structure.  
For each page and component you have separate Go structure and template definition.  
You can inlcude data fetching and display logic just right inside of a component.  
Second thing I provided is page rendering lifecycle.  
This allowed me to solve asynchronous calls issue.  
You can implement async method for component and it will be called with own goroutine under the hood on page rendering.  
As an example, you have 10 instances of the component on the page.  
In that situation 10 goroutines will be created for each asynchronous call.  
And the most interesting thing in this library I've implemented is a built-in dynamics functionality, inspired by Hotwire and Laravel Livewire.  
It's pretty simple and limited because it's created for simple things.  
But people really liked it, and I'm extending functions over the time.  

# Slide 7

As the project has solidified its core idea, I'm able to make some plans for the future.  
We already working on UI Kit, based on Tailwind UI and already using it for our internal tools.  
Anyway, it still needs a lot of work.  
Also, one of the features I'd like to provide is a Server Side State.  
This approach will allow to reduce initial amount of transfer data between server and client.  
And last, but the most interesting and crazy idea I'm experimenting on is bringing the whole rendering process to the Edge Workers.  
It's giving to us a serverless setup and insanely fast responses.  
Unfortunately, Cloudflare Edge Workers have a lot of restrictions (like 1 MB executable limit) and don't have official support for Go.  
I was able to run Go on the Edge Workers with tinygo compiler, but it's not enough to be able to use kyoto as expected.

# Slide 8

So, here is a quick summary for this talk.  
I think Go have a big potential and is not limited by current domain.  
Otherwise, it would be impossible to create tools and libraries like this.  
I'd like to note that kyoto is not a framework by it's own.  
On my opinion, combination of UI Kit, project blueprints and best practices are actually become a framework.  
I'm not creating kyoto opposite to JavaScript solutions.  
Even more, it's possible to integrate them.  
I just believe that every solution has an own purpose.  
And I hope this solution will help someone too.  
You can find all needed links on this slide.  
Dont hesitate to contact me directly anytime.  
And that's all from my side for today.  
