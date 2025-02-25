# Data Ethics Club discusses [The mathematics of crime and terrorism](https://www.youtube.com/watch?v=lCjspXB5F4A) (14th July 21)

```{admonition} What's this? 
This is summary of Wednesday 14th July's Data Ethics Club discussion, where we spoke and wrote about the YouTube video [The mathematics of crime and terrorism](https://www.youtube.com/watch?v=lCjspXB5F4A) by Hannah Fry.

The summary was written by Huw Day, who tried to synthesise everyone's contributions to this document and the discussion. "We" = "someone at Data Ethics Club". 
Nina Di Cara helped with a final edit.
```


## Introduction

This week's content was a Numberphile video entitled ["The Mathematics of Crime and Terrorism"](https://www.youtube.com/watch?v=lCjspXB5F4A) from February 2016, featuring Dr Hannah Fry, a Senior Lecturer at UCL's Centre for Spatial Analysis. In the video, Fry introduces the idea of modelling independent random events (the example given was horse kicks leading to the deaths of soldiers in the Prussian army). 

Fry points out that acts of crime and terror are not independent and so a statistical model describing these events would have to have some sort of dependence between events. A good example of this is the idea of repeat victimisation. If your house is burgled, you are your neighbours are much more likely to be burgled from again in a very short space of time, as the perpertrators are more familiar with the area. This is analogous to the aftershocks of an earthquake.

A Hawkes process is a type of stochastic process which can be used to describe such patterns, and Fry introduces this process as a way of modelling incidents of violent crime and terrorism, as shown in a paper she co-authored with one of her PhD students: [Spatio-temporal patterns of IED usage by the Provisional Irish Republican Army](https://static1.squarespace.com/static/549d680ee4b0bf1b6a956794/t/56b096e7f8baf3fe2ec9280c/). In this paper a unique dataset of improvised explosive device (IED) attacks during “The Troubles” in Northern Ireland (NI) is analysed via a Hawkes process model. 

As well as being used retrospectively, such methods are being used predictively, including by a company called [Predpol](https://www.predpol.com/). In this Data Ethics discussion, we debated the ethics of such tools, what value they can bring and whether it's a good or a bad thing that such models aim to cut out the emotion from decision making.

Author's note: this is a discussion launched off a 10 minutes youtube video designed to be accessible to a general audience, with a focus on the technical side of the work, not on the ethics. The video is from several years ago and with a shift in the way law enforcement is viewed in recent years, it would be counterproductive to judge the thoughts of someone 5 years ago through today's lens. In Dr Fry's more recent writing "Hello World: How to be Human in the Age of the Machine", she touches on some of the ethical concerns surrounding this type of analysis, including in her own work. The below discussion flowed frequently between the underlying maths, the application of the model and the way in which the model was marketed.

## What ethical concerns do we have about predictive policing?

The main ethical concerns we had are the social aspects that are not considered using tools (socioeconomic backgrounds for example). What is this tool really predicting? This follows a pattern of algorithms which have been mentioned in previous discussions (as well as in books such Automating Inequality and Weapons of Math Destruction) where a lack of sufficient resources is compensated for with some clever tech fix that decides how to distribute such resources. 

Indeed on [Predpol's website](https://www.predpol.com/roi-predpol-white-paper/) there is a section of marketing, justifying an investment in their work "How did a PredPol customer get the equivalent of 16 new officers and recoup its investment in less than one month?" Such marketing might appeal in an "us vs them" environment, where crime is scene as one side of a battle being fought on a "thin blue line". This fails to recognise the social aspects of crime, as we discussed later.

Many of us felt generally uneasy about these model, but don't necessarily know how to atriculate the statistics of why. It's important to think about the assumptions we are making with models, even though we probably can't list them all. 

Could there be feedback loops in this model? If police patrols increase in an area, more arrests happen there - could that then feed data in and continue to patrol there? Whilst this concern is valid, as we understand, Predpol only relies on victim reports, not on arrest data to fuel their analysis. This leads to interesting ideas about the difference between arrests and victim reports and the possibility of disparities in these victim reports. White collar crimes might be less likely to be reported, so any such algorithms fueled by victim reports, is likely to target a specific part of the population.

The ethics of this system (and law enforcement in general) depends very much on the consequences of what you're predicting and how you react to it. There's an implication in this video that you can adjust the probability (by reducing crime) over time. It took it as a given the "underlying randomness". It would be interesting to investigate that a bit more. While Predpol claims to have been able to reduce burglaries by up to 32% in certain areas, it's important to note that some trials of Predpol found found no difference at all.

## Is statistical modelling “free from emotion and hand-wavey-ness”?

In the video, Hannah Fry makes a claim that the process of modelling is "free from emotion and hand-wavey-ness". To the general audience of Numberphile (those enthusiastic about maths and its applications), this is quite an appealing idea. Indeed, if we fix solve difficult problems without having to worry about it, surely that would make everyone's lives better? Well, it depends on the fix. Perhaps a better question to ask is whether using mathematics in this way is a good way for mathematicians to try to help people?

The culture of solving well-defined problems in mathematics encourages a focus on narrow aspect of the problem (reductionism). There is a culture in mathematics of solutions not being useful for 100s of years, so you can see why mathematicians don't always ask "is this useful?" before applying maths. But in a situation like this, mathematicians aren't solving the underlying problem (why is crime happening), you're just modelling the process. Even by doing the research you are creating "subjects". Researchers have a responsibility to be ethical in how they treat these subjects.

So we can forget these are humans? Human with context and environments, embedded in systems etc. Of course not! Context is vital. Remembering these are humans is vital. Crime is not just a number that needs to be reduced. It's real people, some making poor decisions, some forced to make such decisions by the environment they are in. Do we need to treat these criminals as problems to be solved (i.e. arrested) or as people in need of society's hope? (Maybe this is the hand-wavyness Dr Fry was alluding to!)

Mathematicians often think just because we have an equation to describe something, it's objective and not subjective. We need to be more assertive in stressing that this is not the case: models are not free from emotion. The idealistic goal of this sort of work is to observe the real world in a way which is completely unbiased. As social beings fomulating social problems that is not going to possible, so we need to be mindful of the impact we might have. 

For instance, we aren't the people who will be using the model at the end. Even if we think we are perfectly ethical, not everyone will use our outputs with the same ideals. How much might we be leaving up to the interpretation of the people who use it? And what might that mean for those on the recieving end?

## What impact do you think predictive policing is having on crime?

As with algorithms applied in many other industries, sometimes if you're getting the wrong answer, you might want to ask a different question. If the success of this system is predicated on number of arrests, then more pings indicating where police should patrol, will lead to more arrests which will lead to a "job well done." Perhaps instead we should be asking, "is this solving some sort of societal problem?" 

This problem happens in a lot of industries but is somehow worse in policing because of the severe impact this has on lives. A single arrest can lead to an unfavourable sentence by a potentially biased judge. This sentence has a knock on effect for life, with decreased job prospects and social stigma, frequently leading people back to crime. With reoffending rates so high, is it really a job well done if more people get arrested (particuarly for less severe crimes), leading to higher reoffending? If this means arrest rates get higher in the long term, all the better (for Predpol).

Now of course, this system is not the fault of the algorithm, it was here long before any Hawks process model. But given the confines the model is operating in, perhaps it would be wise to take a step back and ask "how can we help solve a societal problem?" instead of treating crime as a probability to be arbitrarily lowered.

Predictive policing isn't the only approach to this "issue" which is flawed. As documented in the film Coded Bias, police in the UK are using mobile surveillance vans to scan crowds with facial recognition software. They're treating facial imagery like fingerprints, using a possible match as grounds for arrest. The main difference is that they're collecting the data at will, without consent from those present. Results with this method varies, with many false positives.

If attempts to use machine learning to detect scammers online  wrongly classified you if you mispelled your name or password, is that ever acceptable? Should we play it safe and not try to use these methods if there is a risk for things to backfire? Similarly, if in some areas, burglaries were reduced by as much as 32%, should we deny the residents of those areas that, just because of the inherent issues in the system? On the other hand we also have to ask what our acceptable rates of error are. Are any false positives acceptable in this use case?

For example, certain neighbourhoods with lots of undocumented citizens in the US are less likely to report crime. By not using these predictive policing tools, are we avoiding helping the victims of crime? By not implementing these systems are people missing out on protections we could provide them? If we're not careful, in our quest to avoid discrimination with such tools, we might end up discriminating against neighbourhoods where the tools make a real difference.


## What should happen as a result?

We would like to see more people acknowledging that these social problems are complex and multi-dimensional. Blindly applying algorithms without thinking through how the numbers would be used could turn a lot of rough sleepers into criminals. Perhaps rather than treating the outputs of such models as suggestions on where to send arrests, it should encourage community outreach initiatives. If there's a problem area, why is it a problem area and what can we do about that (instead of just applying a zero tolerance policy)? The debate on how to use information on crime has been had already in the context of [Broken Windows Theory](https://en.wikipedia.org/wiki/Broken_windows_theory).

Governments have the main power to change this, but perhaps not the will. Debates are happening in both the UK and the US about how police should interpret laws. Lockdown is a good example of this; there have been different responses by different police forces in the UK over violations of laws and guidelines. Accountability over these responses, as well as better guidelines on how the responses will help both consistency in treatment as well as shaping a more consistent approach - for better or for worse. 

Mathematicians and other academics have both the power and the responsibility to change this by by acknowledging the limitations on the work that we do. This is an uphill battle in an environment fueled by grant applications but as we've seen in the past, relying on personal responsibility of individual academics is simply not sufficient. 

Some people might come out of watching this video and think "this approach is amazing and can fix all the problems". The video likely should include the social limitations in the conversation. Some might make the argument that the content of the channel is intentionally apolitical, but as is often the case, being apolitical ends up advocating for the current (however unjust) status quo.

The actual companies implementing these systems, going from academic theory to real world application, of course hold responsibility. Unfortunately, as with academia, acknowledging flaws and limitations in a system is not good marketing. Part of this is likely optimism that they can fix these issues, but part of it is wilfull ignorance about the complexity on these issues. 

If those in industry are only interested in profit and the best way to make profit is to not be ethical, then we cannot rely on them to be ethical by choice. It can sometimes be fashionable to be ethical (as it can be fashionable to have a rainbow in your company logo for a month, but not a day later). We need to somehow make it in their best interest to be ethical. This links back to those in government, requiring policy makers to set regulations that restrict how we use this sort of technology. As we saw in Coded Bias, law enforcement will be resisitive to this change, preferring no external accountability. This will be an uphill battle as policy makers are the main clients for companies like Predpol.

It's not all dreary in the future. It would be jumping the gun slightly to attribute all of the actions of those involved as malice. The idea of reducing crime is a noble one, even if the approach is flawed. If we assume all those acting are malicious, then the battle to restrict how they act is great. If we more optimistically suppose than many in this field are acting with misguided but otherwise good intentions, more productive discussions can take place and the battle to curb the automitation inequality starts looking a lot more winnable - especially as a younger, more ethically aware generation starts joining the ranks in industry, policy making and academia.

---

## Attendees

Note: this is not a full list of attendees, only those who felt comfortable sharing their names.

__Name, Role, Affiliation, Where to find you__
- Natalie Thurlby, Data Scientist, University of Bristol, [NatalieThurlby](https://github.com/NatalieThurlby/), [@StatalieT](https://twitter.com/StatalieT) 
- Nina Di Cara, PhD Student, University of Bristol, [ninadicara](https://github.com/ninadicara/), [@ninadicara](https://twitter.com/ninadicara)
- Huw Day, Maths PhDoer, University of Bristol, [@disco_huw](https://twitter.com/disco_huw)
- Sergio Araujo-Estrada, RA, University of Bristol
- Dan Gorringe, Research Engineer Intern @Hadean (and Bristol Grad), [@DanGorringe](https://github.com/DanGorringe)
- Kamilla Wells 

14 people attended the discussion in total. 
