# The Luck of the Procrastinator, or How I Spent My Fall Vacation.

Like most; I’m inundated with email, the day before Chipy's Fall 2018 Mentorship Program application deadline, a subject line caught my eye. Last Chance! I thought, if this is my last chance, how on earth did I miss my first? I clicked to learn all about it, and without hesitation, I thought "Why not?" I had no great expectations I'd be selected. I find great expectations often lead to severe disappointment, it's the mantra which supports my flight-by-seat-of-pants lifestyle. When I received the acceptance email, I was pleasantly surprised, until it sunk in seconds later...there go my lazy fall afternoons playing Skyrim. But it's exactly what I need, structure—I need method to my madness.

I've been working with data for the last 15 years or so, and currently use SAP/BW, SQL Server, Informatica and Tableau at my job. My CS curriculum was in Java, but I haven't used it much since graduating. I've been dipping my toes in Python and R for data cleansing, and planned on exploring Python for automation, pipelining and testing for the ETL we do at my company. Chipy’s program came to my attention at an opportune time, since I struggle to make headway without an end goal during my free time. We use enterprise tools at my job, so I explore open source on my own time. I've never had a mentor, unless you count my keyboard. It’s not very responsive, and makes no-sense when I bang my head against it. Passing along what I've learned has always brought me great satisfaction, so I figured it is my duty to pay it forward to some lucky mentor.

## So here goes nothing, or Dear Diary (Project Management Edition) 

### Kickoff Dinner 8/27/18

Chipy hosted a kick-off dinner for the start of the program. Again, I didn't know what to expect. There was no order to the mix-and-mingle; we sat, ate and great conversation ensued. Ever so often, the program managers would switch us around, and we'd continue. Midway, we stopped to receive a rundown of the program, after which we could stay and get to know our fellow cohort some more. I got a chance to meet my mentor. I briefly mentioned my conundrum, should I do a fun project, or should I do a practical project? The pragmatic in me won, and I decided to solve a data problem, which has been bugging me at work for quite a while. I was familiar with the domain, and I knew I could work on it incrementally. It was a project with a doable minimum viable product I could do within the timeline. I'm also trying to learn R and then there are the video games...sssshhhh, our secret :wink: It was also a project that would touch on most of the things I need to dive deeper on in order to continue my work after the program ends--Python, Pandas and Notebook, Oh my!

### Week 1 9/3/18 Monday, Sept 3 Mentor/Mentee 1-on-1

Agenda: Discuss New Product Development & Vitality Index Project 

Discussion: I met Jim J. at the agreed upon bat time and channel to go over "The Project." Ah, it seemed so simple at the time. In my experience, once you start coding logic, the wrenches start flying, but I have honed the skill of dodging wrenches. I felt we were in a good spot, one of the benefits of picking a practical project is less time is wasted agonizing over what data set to use or what questions to ask and answer. I like to pace myself; for a procrastinator, I am extremely disciplined under pressure. One of my favorite thoughts on learning is by yo-yo ma, something along the lines of learning incrementally and consistently, makes learning fun and painless. Um, does this apply to coding?
Phase 1 - Data Pipeline

Minimum Viable Product:
De-dup a dataset of materials based on a set of criteria for N rolling years.
Include records where first instance Previous Status = New & New Status = Active
Exclude records where Previous Status = Null
Exclude records where last instance New Status = Inactive | Discontinued
Create Python Script: Arguments - Date (N Years) Materials.csv, Purchases.csv, Exclusions.csv
Calculate Vitality Index
Blog Medium | Notebook on Github Can you guess which one won?

Phase 2 Data Validation

Phase 3 Visualization

Phase 4 UI

Python script | Executable | Web Service/Web part on SharePoint

Phase 5 Data Integration


Next Steps: Get familiar with Anaconda Nav, Notebook & Pandas
Deliverables: Set-up Anaconda, Python 3 Environment, Create Project Notebook & Explore dataset using Pandas
Resources:
[Brandon Rhodes - Pandas From The Ground Up - PyCon 2015] (https://www.youtube.com/watch?v=5JnMutdy6Fw)
[Kevin Markham - Using pandas for Better (and Worse) Data Science - PyCon 2018] (https://www.youtube.com/watch?v=0hsKLYfyQZc)
[IPython and Jupyter in Depth: High productivity, interactive Python - PyCon 2017] 9https://www.youtube.com/watch?v=VQBZ2MqWBZI)

### Week 2 9/10/18 Monday, Sept 10 Mentor/Mentee 1-on-1

Agenda: Discuss Week 1 Next Steps and Deliverables

Discussion: We trouble-shooted publishing the project notebook on Anaconda cloud. I love Anaconda, it's the next best thing since sliced bread! It lets folks dive right into coding without the barrier and headache of setting up your environment and getting your libraries to work. We coded the first condition in Pandas, "Include records where first instance Previous Status = New" and called it a day.

Next Steps: Start working on Blog 1

Deliverables: Share notebook on Anaconda Cloud & continue coding criteria. 

Resources:

Thursday, Sept 13 ChiPy (optional)

Deliverables: Head-shot Due

### Week 3 9/17/18 Monday, Sept 17 Mentor/Mentee 1-on-1

Agenda: Discuss Week 2 Next Steps and Deliverables

Discussion: While exploring the data I realized I was overthinking some of the criteria. Since the first step was to identify materials, which had become active at some point, I didn't need to worry about the previous status. The issue with identifying NPD materials is that the creation date in SAP can happen much earlier to the time when a material becomes sellable, i.e. is in active status. To further complicate things, the material status can flip-flop throughout its lifetime. Materials which have been discontinued or were inactive, can be resurrected—these I refer to as zombie parts. We have a BW table that is written to any time the status changes, materials are hence, almost duplicates (except for the change date), which means they are slightly unique. We later found the other condition, exclude materials whose current status in inactive or discontinued, contained materials which were never activated in the first place, go figure. We also reviewed reading the date fields in the csv as dates; we would need them to be dates once we coded the N Rolling years part, and also to de-dup based on the earliest date, and exclude based on the latest date.

Next Steps: Explore the to_datetime method, continue working on Blog 1

Deliverables: Work on reading the date fields as dates 

Resources: https://talkpython.fm/episodes/show/156/python-history-and-perspectives

To be continued…
