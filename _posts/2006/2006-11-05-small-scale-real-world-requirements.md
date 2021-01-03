---
title: "Small Scale Real-World Requirements"
date: 2006-11-05 18:09:53
year: 2006
---
Over the past couple of weeks, I've had some interesting conversations with local small software companies about their development process---in particular, about how they collect and manage requirements.  It isn't anything like it is in the textbooks, and I think I may have figured out why.

Here's one web development company's process:
<ol>
	<li>A technical salesperson interviews customer to find out what the customer wants.  For the most part, this consists of checking off items on a spreadsheet: "User self-registration... Mailing lists... Blog feeds... Product overview pages... Product pages...  Got it."  There may be a few "custom components" in the mix, but for the most part, the customer's web site can be assembled by customizing and combining off-the-shelf components.</li>
	<li>The salesperson estimates the size and complexity of the job on a small/medium/large scale.  This selects the scaling factors that are applied to the individual work items, the basic implementation time of which is built into the spreadsheet.  The salesperson also estimates the time required to build any custom components, usually by analogy with similar items done previously.  What comes out the end is a preliminary estimate of the project's cost.</li>
	<li>This estimate is taken back to the customer, who is then told how long it will take to firm up the design (a necessary step toward getting a final cost).  If the customer says, "No thank you," the two sides shake hands and go their separate ways.  Otherwise, the company works on a time-and-materials basis to turn the rough estimate into a design detailed enough to form the basis of a contract.</li>
	<li>The finished design is taken back to the customer---in fact, it is the customer's property.  If the customer wants to take it elsewhere for implementation, there's another opportunity for a handshake and a farewell; in practice, though, that has never happened.  What <em>does</em> happen is that customers try to whittle down the price (which usually results in work items being pushed off, since the one thing customers are usually absolutely firm on is deadline).</li>
	<li>The web development company then translates the design into code. Usually, the result is a happy customer, but sometimes the customer looks at the finished product and says, "This doesn't do what we asked for."  This is the point at which it becomes clear that the customer didn't actually read the design document: either they trusted the web development company, or didn't have time, or couldn't make any sense of it.  What follows is usually what the diplomats refer to as "full and frank discussions"...</li>
</ol>
Here are some observations:
<ol>
	<li>The development company has to commit to implementation details very early on in order to tell the customer how much things are going to cost (which in turn shapes the customer's requirements---if you can't afford it, you don't need it).  This is at odds with textbook approaches, in which you figure out what the customer wants, then figure out how you're going to build it.</li>
	<li>The initial spreadsheet isn't nearly detailed enough to give to developers on its own.  Since the customer has already told the development company what it wants, the development company can't let its programmers go back and re-interview the customer to flesh the spreadsheet out (double cost to the customer, and it would look unprofessional).  The technical salesperson who spoke to the customer therefore has to dump everything s/he knows into to the mind of whoever is going to work up the detailed design as quickly and accurately as s/he can.</li>
	<li>The detailed design is done in terms of features: this page has widgets with these capabilities, that database stores information according to such and such a schema, and so on.  Customers, on the other hand, think about what they're buying in terms of a muddled mix of pages and business processes: pages, because using the web has trained them to think that way, and business processes, because they want the web site to <em>do</em> something.  Mapping the customer's stew to a feature list is hard; mapping the features back to the stew in a way that the customer can understand is close to impossible.</li>
</ol>
Why does this company do things this way?  Because any other methodology would lead to bankruptcy.  If you're IBM or Arthur Anderson, and the job itself is going to take five years and cost forty million dollars, customers will pay for your up-front design time (which may well be six months or a year).  Customers will <em>not</em> pay for the up-front on a two-person, six-week web site upgrade (in part because the kind of customer who needs that kind of job done usually isn't particularly clued in technically).  You have to figure out what the job's going to cost to make the sale; you need to know how you're going to build it to figure out what it's going to cost; so you need to turn stew into implementation features much earlier than purists would have you do.

Another interesting observation is the way that this process steers development companies (not just the one whose process is outlined above) in certain directions.  The more you standardize your offerings, the better you will be able to estimate costs.  Whether it's web site development, telecoms, or data analytics, small companies doing on-demand work all seem to try to componentize their offerings in order to avoid losing their shirts.

Finally, none of the people we've spoken to so far have much time for <a href="http://www.extremeprogramming.org">Extreme Programming</a>.  Customers need to know what they're going to get months ahead of it being delivered, so that they can firm up all their other plans.  If purchasing tells marketing that the spec is, "We're giving them money, and they're going to satisfy our needs," someone's gonna lose their job.  The only exception is when the development company has built up a lot of trust with the customer; if the developers have delivered above and beyond several times running, the customer may well say, "Here are the keys, take it away."

Here are the takeaways:
<ul>
	<li>In order to succeed in the real world, a development process for small and medium-sized teams has to allow those teams to determine the time and effort a job is going to require very early on.  That in turn requires a "leap to implementation", with all the concomitant risks of focusing on plumbing at the expense of decor.</li>
	<li>Companies want a lightweight, dynamic way to manage requirements. One idea (which we've heard twice) is to file a ticket for each requirement, then link those tickets somehow to the "feature to be implemented" tickets that satisfy it.  Such a system would also need to allow its users to impose an order on those tickets, so that they could be run off as a single, coherent document.  (Don't groan---what's important here isn't the paper, but a sensible linear ordering.)  This ties in nicely (we think) with adding parent/child relationships to tickets to help with scheduling ("X can only be started once Y and Z are finished", and so on).</li>
</ul>
Thesis topic, anyone? ;-)