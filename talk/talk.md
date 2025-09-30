
A Data Flow Perspective on “AI Social Simulation”: Will Recent AI Advances Enable New Social Science, Destroy Ecosystems for Knowledge, or something More Subdued?


Abstract: In this talk, I will connect prior work on “data leverage” (collective action and collective bargaining with data) and recent discussions of online communities as “content ecosystems” for AI training data with in-progress work critiquing the use of “AI Social Simulation"

Key points I really want audience to convey:

- #1, a prediction: as the title suggests, the overall impact of AI / LLM Social Simulation will indeed fall somewhere in between the extremes of enabling a golden age of social scientific discovery vs. completely destroying any and all epistemic communities.
- #2, a policy argument: There are a number of reasons to advocate for increased transparency around LLM training data. While I'm highly interested in these arguments, I want to argue that social science as a broad community should argue for this on purely epistemic grounds. Many of the concerns around LLMs can be mitigated by improving transparency at three points in the pipeline: dataset selection, mechanistic interpretability, and AI auditing
	- Three concrete paths to do this: 
		- convince all our friends at tech companies!
	- 
- #3: raising some of the other critiques around AI, in case they make for a generative discussion.

Some recent works I'll use to ground this talk

Specific works I'll mention in this talk:

- An Audit and Analysis of LLM-Assisted Health Misinformation Jailbreaks Against LLMs
	- Ayana Hussain, Patrick Zhao
		- (Exciting: first author by undergrad. I saw this when working in Amy's lab)
	- Key idea: LLM can be very good at generating jailbreaks against other LLMs, and then doing detection on these very jailbreaks. How can this all be true at once?
- In-progress work from students (Patrick Zhao -- awesome Msc up in Vancouver, always keen to meet more folks in this area -- he's from CS and I promised as part of my "rescheduling-advising meeting" to find some social science folks to chat with at some point)
- My main shtick: current AI products are massively data-dependent. This means they are very difference than other technological advances -- there's a true collective dependence, in the sense that we can imagine many counterfactuals where people change their behaviour and make AI worse
	- imagine a world without wikipedia
	- or people stop using thumbs up in ChatGPT
	- or people stop posting on Facebook
- we (a broad we -- computing, computational social science, etc) should support collective action around data so various communities can wield "data leverage"
- Data leverage can be broadly applied to many causes, including those I don't personally agree with
- One area of personal interest for me is specifically collective bargaining for information to cushion economic shocks from automation of knowledge work / more generally prevent concentration of power by the winners in the AI Race
	- Works
		- Recent: CBI position paper @ NeurIPS pos paper track (would love feedback; camera ready due October 23 :D )
		- Older: data leverage
		- Empirical and simulations work on studying specific instances of collective action (how much can group x impact AI model y in terms of performance metric z)
			- Have a whole workshop at NeurIPS this year. woohoo!
	- Also, FYI, if anyone here is connected: I'm REALLY keen to connect with Bluesky folks. Had a great discussion at FAccT this year about atproto and these topics.
- A second area of interest of mine is figuring out how to enable "public AI" -- models that are built, deployed, governed by a consortium of public bodies (national AI institutes, but also states, state-wide university systems, etc.)
	- See publicai.network, publicai.co for our live product (while compute donations we scrounged up last)
- A third area of interest (highly related): preventing scenarios where AI technologies hurt the "content ecosystems" on which they are reliant (shout out CDSC work on ecology line of work on online communities; Mako, Nate, Jeremy, Sohyeon, maybe other current students I'll chat with after)
	- Hypothesis goes like this, you've probably heard it by now: AI substituets for use of Wikipedia / SO / etc. People stop going to Wikipedia. Volunteer energy "dries up". New AI models get worse because Wikipedia is no longer up to date. feedback loop effectively wipes out certain communities.


So:
- Data leverage / CBI: AI depends on data, so we can threaten to withhold, modify, redirect to allow data creators (either small groups of specialists with very high leverage data or large groups of general users)
- Public AI: we should get public bodies to deploy AI. They will have disadvantages, but are also well-suited
	- Public AI more likely to deploy transparent / open models, it seems (thus far)

Ok, now I promised that these would connect to AI Social Simulation and Social Science.

---


- The current state of affairs for LLM Social Sim is that a lot of work is stuck proving that they can produce a set of phenomena rather than how they can arise
    

- E.g. Many papers have the research question: “can, or how well can LLM agent simulation produce this behavior” rather than the end goal of studying how the behavior is produced, how it might change with interventions, etc.
    
- Larooij et al. surveyed contemporary LLM ABM literature and found that most metrics focus on “believability” as an eval (human or LLM as a judge)
    

- [https://arxiv.org/abs/2504.03274](https://arxiv.org/abs/2504.03274)
    

- In the simulation literature the ability to produce patterns accurately refers to “dynamical sufficiency”, how well a simulation can capture the dynamics of a target phenomenon.
    

- Consider: plotting a curve accurately without necessarily
    
- People were excited because LLMs seemed to move us further up the “dynamical sufficiency scale”, allowing our agents in ABMs to have a larger action space.
    

### Thought 2

- Suppose we want to know “how” or partially how a phenomenon might have arisen. Mechanists argue that any level of explanation requires us to map the model’s components and activities to the hypothesized “real” components and activities.
    

- If a model is only concerned with whether or not the behavior is produced accurately, it is a “phenomenal” model.
    

- Importantly, for practical social simulation, if we want to test interventions we are trying to model unknown counterfactual scenarios.
    

- This is related to mechanisms rather than dynamical sufficiency. 
    
- Gap: 
    

- papers evaluate or justify using sufficiency/believability, but then test interventions as if there are plausible mechanisms
    

### Thought 3

- As a community we need to consider: can we do LLM sim with closed models? Those accessed by API?
    

- Safety guardrails could alter agent behavior mid-experiment or between runs
    

- version updates, guardrails, safety filters, hidden prompt injections
    

- The problem is solvable with offline models. But 35 out of 35 papers surveyed used an API of some sort
    

- GPU/technical constraints
    

- Even more technical approaches to evaluation, things like checking if distribution of answers match, still is "phenomenal".
    
- Additionally, mechanisms can be stochastic. But if they need to be deterministic we should consider that LLMs may not be deterministic in practice even if we set the seed/temperature to be the same every time.
    

- There has been work on “defeating non-determinism”
    

- Everything just needs to happen on the same GPU instead of being split up. If we do this then our outputs are deterministic.
    
- [https://thinkingmachines.ai/blog/defeating-nondeterminism-in-llm-inference/](https://thinkingmachines.ai/blog/defeating-nondeterminism-in-llm-inference/)
    

- For API access, this is not possible because it is almost certain that large providers are splitting the operations across multiple GPUs
    

### My Current In-Progress Work

- Motivation: simulation epistemology seems to be confusing and a shared pain point across many projects. Too much historical work on modeling (not just ABM) to catch up on 
    
- A scale/axis for measuring “mechanism plausibility”, increasing as more parts of the model are falsifiable. Reduces overhead of needing domain knowledge from philosophy of science
    

- To be falsifiable, there needs to be a claim/hypothesis put forward. In LLM social sim this could be referring to the target phenomenon
    
- S T I E:
    

- Level 0: you have a simulation S with no operationalized target. 
    
- T, target phenomenon needs to be operationalized to be falsifiable (level 1)
    
- I, intent. Mapping of what mechanisms the components/organization in the simulation represent.(level 2)
    
- E, evidence. The evidence supports how other parts like S, T, I are chosen and operationalized, but also can be falsified / countered. (level 3)
    

- Each level is a prerequisite for the next.
    
- NOTE: HIGHER LEVEL /= STRICTLY BETTER SIMULATION
    
- By evaluating your own sim using this it is an easier way to think of all the background stuff I just talked about.
    
- I will talk in my main paper what are the implications of each level, what are the epistemic contributions for different simulations. 
    

  

### Contact Me:

- [pza28@sfu.ca](mailto:pza28@sfu.ca) or [patrick123cool@gmail.com](mailto:patrick123cool@gmail.com) 
    
- Happy to collab on more practical / grounded simulation projects as well as abstract ones like this