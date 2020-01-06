## The future of GATK tutorials is written in Jupyter Notebooks

By Geraldine_VdAuwera

<p>Last week I wrote about how we're using a cloud platform called <a rel="nofollow" href="https://app.terra.bio">Terra</a> to make it easier to get started with GATK; and specifically I highlighted the <a rel="nofollow" href="https://app.terra.bio/#library/showcase">fully loaded workspaces</a> that showcase our <a rel="nofollow" href="https://software.broadinstitute.org/gatk/best-practices/">Best Practices pipelines</a>, which we think will make it a lot easier to <a rel="nofollow" href="https://software.broadinstitute.org/gatk/blog?id=24139">test drive our pipelines end-to-end</a>. This week I want to talk about a complementary approach we're taking, using Jupyter Notebooks on Terra to teach the step-by-step details of what happens <em>inside</em> the pipelines. Though before we get into the nitty gritty of how it works, I'd like to take some time to walk you through why we're taking this particular approach.</p>

<p>Writing a good tutorial is not that hard, in theory. You state the problem, provide a command line, then give a few instructions for poking at the outputs and you discuss what happened. The hardest part should be choosing what details and parameters to explain vs. what to leave alone to avoid confusing newcomers. Right? Well… In practice, the hardest part is often providing the inputs and instructions in such a way that most people will be able to run it in their own, unique and precious computing environment without some amount of head scratching and at least three pages of alternative instructions for this system or that system. Ugh.</p>

<p>We've run dozens of workshops where the setup is that we provide a PDF of instructions and a data bundle, and participants run commands in the terminal on their laptops. Inevitably some non-trivial amount of time ends up being spent debugging environment settings, typos and character encodings. That's just not a good use of anypony's time. Plus we want to be able to demonstrate larger-scale analyses with full-size inputs, not just the usual snippets of data whittled down to be convenient to download and move around. (Genomic data is getting big, if you haven't noticed.)</p>

<p>So earlier this year, we converted all our workshop tutorials to Jupyter Notebooks, an increasingly popular medium for combining live, executable code and documentation content, hosted on <a rel="nofollow" href="http&quot;//app.terra.bio">Terra</a>.</p>

<p>And no kidding, it's been <em>transformative</em>. So far this year we've done three "GATK bootcamp" workshops (4 days long, 50% hands-on tutorials) and in every one of them the verdict was the same: notebooks FTW. Compared to our old approach, we spend so much less time troubleshooting technical issues and so much more actually exploring and discussing what the tools are doing, what the data looks like and so on -- you know, the interesting stuff. Not unexpectedly, the Notebooks-based approach is also proving to be extremely popular with participants who have less experience with command line environments.</p>

<p>In my next post later this week, I'll walk you through one of the notebooks from our most recent workshop. My goal is is to show how you can take advantage of these resources to level up your understanding of how GATK tools work even if you can't make it to one of our workshops in person.</p>

<p>Of course if you're too impatient to wait for the guided tour, feel free to sneak a peek at the notebooks I plan to demo, which you can find in <a rel="nofollow" href="https://app.terra.bio/#workspaces/help-gatk/GATKTutorials-Germline-June2019">this workshop workspace</a> in the <a rel="nofollow" href="https://app.terra.bio/#library/showcase">Terra Showcase</a>. If you read <a rel="nofollow" href="https://software.broadinstitute.org/gatk/blog?id=24139">my post on the Best Practices pipelines</a> from last week, you might have already signed up on Terra and claimed your free credits… but if you haven't, please go ahead and do that now, because you're going to want to clone the workspace and open the notebooks in interactive mode.</p>

<p><em>Go to <a href="http://app.terra.bio" rel="nofollow">http://app.terra.bio</a> and you'll be asked to log in with a Google identity. If you don't have one already, you can create one, and choose to either create a new Gmail account for it or associate your new Google identity with your existing email address. See <a rel="nofollow" href="https://support.terra.bio/hc/en-us/articles/360028235911">this article</a> for step-by-step instructions on how to register if needed. Once you've logged in, look for the big green banner at the top of the screen and click "Start trial" to take advantage of the free credits program. As a reminder, access to Terra is free but Google charges you for compute and storage; the credits (a $300 value) will allow you to try out the resources I'm describing here for free. To clone a workspace, open it, expand the workspace action menu (three-dot icon, top right) and select the "Clone" option. In the cloning dialog, select the billing project we created for you with your free credits. The resulting workspace clone belongs to you. Have fun!</em></p>