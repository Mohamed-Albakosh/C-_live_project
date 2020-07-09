<h1>C#_live_project</h1>
<p>For the last two weeks of my time at the tech academy, I worked with my peers in a team developing Web Application in C# using  entity framework code  first. Using Microsoft 
Visual Studio Write code using code completions, debugging, testing, Git management  was a great learning oppertunity for fixing bugs, cleaning up code.During two weeks I worked 
so hard faced some barriers and some problems that I see in first time but in the end I pass and I deliver what was needed on time.  I worked on several back end stories that
I am very proud of. Because much of the site had already been built, there were also a good deal of front end stories  I got a chance to work on that I am very proud 
of.Over the two week sprint I also had the opportunity to work on some other project management like Azure.</p>

<p>Below are descriptions of the stories I worked on, along with code snippets and navigation links.</p>

<h2>Back End Stories</h2>
<ul>
    <a href="#seeding"><li>Seed the database</li><a>
    
</ul>
<div id="seeding">
<h2>Seeding the Database</h2>
<p> this story is to seed the database with the actual data from the Theatre Vertigo website</p>
<pre>
    <code>
    //Seeding database with dummy SeedAwards
        private void SeedAwards()
        {
            var awards = new List<Award>
            {
                new Award
                {
                    Year = 2017, Name = "Drammy", Type = AwardType.Finalist, Category = "Sound Design", Recipient = "Andrew Bray",
                          ProductionId = context.Productions.Where(prod => prod.Title == "Assistance").FirstOrDefault().ProductionId,
                          //CastMemberId = context.CastMembers.Where(p => p.Name == "London Bauman").FirstOrDefault().CastMemberID,



                },
                 new Award
                {
                    Year = 2016, Name = "Drammy", Type = AwardType.Award, Category = "Outstanding Achievement", Recipient = "Scenic Artist,Mindy Barker",
                          ProductionId = context.Productions.Where(prod => prod.Title == "The Drunken City").FirstOrDefault().ProductionId,
                          
                },
                new Award
                {
                    Year = 2016, Name = "Drammy", Type = AwardType.Finalist, Category = "Sound Design", Recipient = "Richard E.Moore",
                          ProductionId = context.Productions.Where(prod => prod.Title == "The Drunken City").FirstOrDefault().ProductionId,
                },
                new Award
                {
                    Year = 2015, Name = "Drammy", Type =AwardType.Award, Category = "Ensemble in a Play", 
                          ProductionId = context.Productions.Where(prod => prod.Title == "Bob: A Life in Five Acts").FirstOrDefault().ProductionId,
                },
                new Award
                {
                    Year = 2015, Name = "Drammy", Type =AwardType.Award, Category = "Direction", Recipient = "Matthew B.Zrebski",
                          ProductionId = context.Productions.Where(prod => prod.Title == "Bob: A Life in Five Acts").FirstOrDefault().ProductionId ,
                },
                new Award
                {
                    Year = 2015, Name = "Drammy", Type =AwardType.Finalist, Category = "Ensemble in a Play",
                          ProductionId = context.Productions.Where(prod => prod.Title == "The School for Lies").FirstOrDefault().ProductionId,
                },
                new Award
                {
                    Year = 2014, Name = "Drammy", Type =AwardType.Award, Category = "Sound Design", Recipient = "Annalise Albright Woods",
                          ProductionId = context.Productions.Where(prod => prod.Title == "pool (no water)").FirstOrDefault().ProductionId,
                },
                new Award
                {
                    Year = 2014, Name = "Drammy", Type =AwardType.Finalist, Category = "Ensemble in a play ",
                          ProductionId = context.Productions.Where(prod => prod.Title == "pool (no water)").FirstOrDefault().ProductionId,
                },
                new Award
                {
                    Year = 2013, Name = "Drammy", Type =AwardType.Award, Category = "Actress in a supporting role", Recipient ="Brooke Calcagno",
                          ProductionId = context.Productions.Where(prod => prod.Title == "Mother Courage & Her Children").FirstOrDefault().ProductionId,
                },
                new Award
                {
                    Year = 2013, Name = "Drammy", Type =AwardType.Award, Category = "Sound design", Recipient ="Richard Moore",
                          ProductionId = context.Productions.Where(prod => prod.Title == "The Velvet Sky").FirstOrDefault().ProductionId,
                },
                new Award
                {
                    Year = 2012, Name = "Drammy", Type =AwardType.Award, Category = "Actor in a land role", Recipient ="Mario Calcagno",
                          ProductionId = context.Productions.Where(prod => prod.Title == "The American Pilot").FirstOrDefault().ProductionId,
                },
                new Award
                {
                    Year = 2012, Name = "Drammy", Type =AwardType.Award, Category = "Sound design", Recipient ="Em Gustason",
                          ProductionId = context.Productions.Where(prod => prod.Title == "The American Pilot").FirstOrDefault().ProductionId,
                },
                 new Award
                {
                    Year = 2010, Name = "Drammy", Type =AwardType.Award, Category = "Supporting Actress", Recipient ="Amy Newman",
                          ProductionId = context.Productions.Where(prod => prod.Title == "God's Ear").FirstOrDefault().ProductionId,
                },
                new Award
                {
                    Year = 2009, Name = "Drammy", Type =AwardType.Award, Category = "Supporting Actor", Recipient ="Garland Lyons",
                          ProductionId = context.Productions.Where(prod => prod.Title == "Romance").FirstOrDefault().ProductionId,
                },
                new Award
                {
                    Year = 2008, Name = "Drammy", Type =AwardType.Award, Category = "Outstanding puppeteering", OtherInfo = "in collaboration with Tears of Joy Theatre",
                          ProductionId = context.Productions.Where(prod => prod.Title == "The Long Christmas Ride Home").FirstOrDefault().ProductionId,
                },
                new Award
                {
                    Year = 2007, Name = "Drammy", Type =AwardType.Award, Category = "Set design", Recipient ="Ben Plont",
                          ProductionId = context.Productions.Where(prod => prod.Title == "Escape from Happiness").FirstOrDefault().ProductionId,
                },
                //new Award
                //{
                //    Year = 2001, Name = "Drammy", Type =AwardType.Award, Category = "Supporting Actress", Recipient ="Andrea White",
                //          ProductionId = context.Productions.Where(prod => prod.Title == "Hellcab").FirstOrDefault().ProductionId,
                //},
                //new Award
                //{
                //    Year = 2001, Name = "Drammy", Type =AwardType.Award, Category = "Supporting Actress", Recipient ="Lorraine Bahr",
                //          ProductionId = context.Productions.Where(prod => prod.Title == "Lion in the Streets").FirstOrDefault().ProductionId,
                //},
                //new Award
                //{
                //    Year = 2001, Name = "Drammy", Type =AwardType.Award, Category = "Supporting Actress", Recipient ="Ted Schulz",
                //          ProductionId = context.Productions.Where(prod => prod.Title == "The Grey Zone").FirstOrDefault().ProductionId,
                //},
                //new Award
                //{
                //    Year = 2000, Name = "Drammy", Type =AwardType.Award, Category = "Outstanding direction", Recipient ="Michael Griggs",
                //          ProductionId = context.Productions.Where(prod => prod.Title == "The Grey Zone").FirstOrDefault().ProductionId,
                //},
            };
            awards.ForEach(award => context.Awards.AddOrUpdate(aw => aw.AwardId, award));

            context.SaveChanges();
        }
    </code>
<pre>
</div>
<h2>Front End</h2>
<ul>
   <a href="#Stylechange"><li>Style chahges</li></a>
</ul>
<div id="Stylechange">
<h2>styling changes</h2>
<p>  Change the style of the page  so that there is always a single Production per row so should displaye verticaly and Change the overlay text font size so that it looks good
at all screen sizes. </p>
<pre>
    <code>
       .currentpro-imgtran:hover {
            transform: scale(1.05, 1.05);
            transform: scale(1.07, 1.07);
            opacity: 0.2;
            z-index: 2;
        }
        .currentpro-text {
            text-align: center;
            position:absolute;
            text-align:center;
            margin-top: -50%;                                                               /*styles text under image*/
        }
        
        .currentpro-fontsize {
            font-size: 1.5vw;
            font-size: 1.05rem;
        }
        @media (max-width:550px){
            .currentpro-fontsize {
                font-size:.8rem;
            }
        }
        .currentpro-txthover { 
            opacity: 0;
        }
        .currentpro-imgtran:hover + .currentpro-txthover {
            
            opacity: 1;                                                                            
        }
       
       <div class="card  col-md-7 mx-auto bg-black">
      
 
          <small style="font-size:.85vw;">
          <small style="font-size:.8rem;">
              
  </code>
  <code>
   
  </code>
<pre>
</div>

<div>
<p>Jumb to: <a href="#seeding">Seed the database</a>, <a href="#Stylechange">Style chahges</a>
</div>
