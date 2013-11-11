manymissions
============

manymissions is a command line tool for producing PDFs with missions that you can cut up and hand
out at parties you're throwing to make them more fun.

You can write a description of your party, for instance:


    party 'db', 30, \
      starts: '7:30pm',
      ends: '9:30pm',
      sites: {
        "in the kitchen" => { starts: '7:30pm', every: '10m', tags: %w{ intimate anywhere } },
        "by the big white wall" => { starts: '7:30pm', every: '10m', tags: %w{ large anywhere } },
        "by the downstairs bathroom door" => { starts: '7:30pm', every: '10m', tags: %w{ rendezvous } },
        "by the front door" => { tags: ['entryway'] },
        "seated on the couches" => { tags: ['seated'] }
      },
      arc: [
        [0.1, 'foreshadowing'],
        [0.1, 'kickoff'],
        [0.4, 'rolling'],
        [0.3, 'risky'],
        [0.1, 'finale']
      ]

And it will pull from a textfile database of missions that look like these:

    large finale // "Slow Dance"
    - shh the crowd   (x3) (-3m)
    - announce its time to slow dance as if everyone were in 7th grade
    - find someone you have a crush on and tell them why.  if you don't have a crush on anyone, pretend you do.   (x10)
    - find the dj and ask for a slow dance  (-3m)

And output a PDF with 10 mission cards on a page.

Enjoy!
