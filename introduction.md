---
layout: page
title:  "Introduction"
---

For more than half a century (from its beginning until the end of 20th-century) software has been developed using a process borrowed from more established disciplines such as manufacturing and construction engineering. This approach, commonly known as [waterfall](http://en.wikipedia.org/wiki/Waterfall_model), is a sequential process, in which every step (analysis, design, development, …) has to be completed before starting the next one.

This methodology may be appropriate to produce bridges or even computer hardware, where building the final product requires much more money and time then designing it and once completed it will not undergo any modification.

However, the same procedure has several downsides when applied to software development where its design is in continuous evolution (features are typically added and changed until the software is retired) and the cost of building the final product (the binary code executed by the machine) is much cheaper than designing it (writing the code that is interpreted or compiled into the binary code).

Moreover, often users may not know exactly what they need before interacting with a working prototype or they may change their requirements from time to time.

Because of all the downsides, during winter 2001 several prominent software developers (among them [Kent Beck](http://en.wikipedia.org/wiki/Kent_Beck), [Martin Fowler](http://en.wikipedia.org/wiki/Martin_Fowler) and [Robert C. Martin](http://en.wikipedia.org/wiki/Robert_Cecil_Martin)) debated alternative methods for software development and, as a result of the discussion, they published the [Manifesto for Agile Software Development](http://agilemanifesto.org).

The first of the twelve principles listed in the manifesto states

{% highlight text %}
Our highest priority is to satisfy the customer through early and continuous delivery of valuable software.
{% endhighlight %}

The Software Development Team at InfoRLife believes the same and it is convinced that, even if waterfall is among the life sciences industry still the de facto[1](#notes) standard, the best way to achieve so is through an iterative process where users are involved throughout the development process and developers follow Test Driven Development (TDD) as the methodology to guide the software design.

This approach to software development not only delivers a better product but it also makes easier, as shown throughout this site, to provide applications that satisfy what U.S. Food and Drug Administration considers software validation to be[2](#notes)

> confirmation by examination and provision of objective evidence that software specifications conform to user needs and intended uses, and that the particular requirements implemented through software can be consistently fulfilled.


#####Notes:
1. De facto because no regulation indicates which development process must be used. For instance, U.S. Food and Drug Administration [General Principles of Software Validation; Final Guidance for Industry and FDA Staff](http://www.fda.gov/downloads/MedicalDevices/DeviceRegulationandGuidance/GuidanceDocuments/ucm085371.pdf) states on page 14: *This guidance does not recommend the use of any specific software life cycle model. Software developers should establish a software life cycle model that is appropriate for their product and organization.*   
2. Page 6 - U.S. Food and Drug Administration [General Principles of Software Validation; Final Guidance for Industry and FDA Staff](http://www.fda.gov/downloads/MedicalDevices/DeviceRegulationandGuidance/GuidanceDocuments/ucm085371.pdf)
