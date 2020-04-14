## What Google learned From Its Quest to Build the Perfect Team
- Many of today’s most valuable firms have come to realize that analyzing and improving individual workers ­— a practice known as ‘‘employee performance optimization’’ — isn’t enough. As commerce becomes increasingly global and complex, the bulk of modern work is more and more team-based.  Research shows that time spent by managers and employees in collaborative activities has grown by 50 percent or more, over the last 2 decades. At many companies 3/4 of the worker's day is spent communicating with colleagues.
- Groups tend to innovate faster, see mistakes more quickly and find better solutions to problems. Studies also show that people working in teams tend to achieve better results and report higher job satisfaction.  Studies also show that profitability increases when workers are persuaded to collaborate more.
- Googles study found:
  - The most productive employees tend to build larger networks by rotating dining companions.
  - That good communication and avoiding micromanaging is critical.
  - They found that understanding and influencing group norms were the keys to improving teams.
    - Norms are the traditions, behavioral standards and unwritten rules that govern how we function when we gather: One team may come to a consensus that avoiding disagreement is more valuable than debate; another team might develop a culture that encourages vigorous arguments and spurns groupthink. Norms can be unspoken or openly acknowledged, but their influence is often profound. Team members may behave in certain ways as individuals — they may chafe against authority or prefer working independently — but when they gather, the group’s norms typically override individual proclivities and encourage deference to the team.
  - What distinguished the "good" teams from the dysfunctional groups was how teammates treated one another. The right norms, in other words, could raise a group’s collective intelligence, whereas the wrong norms could hobble a team, even if, individually, all the members were exceptionally bright.
    1. Conversational turn-taking- As long as everyone got a chance to talk, the team did well, But if only one person or a small group spoke all the time, the collective intelligence declined.
    1. Empathy- The good teams all had high "average social sensitivity" — a fancy way of saying they were skilled at intuiting how others felt based on their tone of voice, their expressions and other nonverbal cues.
- Psychological safety is a sense of confidence that the team will not embarrass, reject or punish someone for speaking up.  It's a team climate characterized by interpersonal trust and mutual respect in which people are comfortable being themselves.

## Web Servers
- Roy Fielding helped write the first web servers, that sent documents across the Internet.  His name is on the specification for the protocol that is used to get pages from servers to your browser.
  - The protocol that he helped write, HTTP, it's capable of all sorts stuff.
    - It tells the browser what protocol to use.
- HTTP is one of the most important breakthroughs in the history of computing.
  - Because it is capable of describing the location of something anywhere in the world from anywhere in the world. It's the foundation of the web. You can think of it like GPS coordinates for knowledge and information.
    - For anything, not just web pages.  
- The whole world wide web is built on an architectural style called “REST”. REST provides a definition of a “resource”, which is what those things point to.
  - Resources are just concepts.
    - URLs tell the browser that there's a concept somewhere. A browser can then go ask for a specific representation of the concept. Specifically, the browser asks for the web page representation of the concept.
    - Are there other kinds of representations?
      - representations is one of these things that doesn't get used a lot. In most cases, a resource has only a single representation. But we're hoping that representations will be used more in the future because there's a bunch of new formats popping up all over the place.
        - There's this concept that people are calling “Web Services” or "APIs". It means a lot of different things to a lot of different people but the basic concept is that machines could use the web just like people do.
- We need to be able to talk to all machines about all the stuff that's on all the other machines. So we need some way of having one machine tell another machine about a resource that might be on yet another machine.
- The way machines tell each other where things are is by URL's.
  - If everything that machines need to talk about has a corresponding URL, you've created the machine equivalent of a noun.
  - Machines don't have a universal noun. Every programming language, database, or other kind of system has a different way of talking about nouns. That's why the URL is so important. It let's all of these systems tell each other about each other's nouns.
- There's a powerful concept in programming and CS theory called ***Polymorphism*** is a way of saying that different nouns can have the same verb applied to them.
  - Some verbs are almost universal like GET, PUT, and DELETE.
HTTP protocol is all about applying verbs to nouns.
  - For instance, when you go to a web page, the browser does an HTTP GET on the URL you type in and back comes a web page.
  - Web pages usually have images. Those are separate resources. The web page just specifies the URLs to the images and the browser goes and does more GETs using the HTTP protocol on them until all the resources are obtained and the web page is displayed. But the important thing here is that very different kinds of nouns can be treated the same. Whether the noun is an image, text, video, an mp3, a slideshow, whatever. I can GET all of those things the same way given a URL.
- Machines basically just need the data. Ideally, every URL would have a human readable and a machine readable representation. When a machine GETs the resource, it will ask for the machine readable one. When a browser GETs a resource for a human, it will ask for the human readable one.