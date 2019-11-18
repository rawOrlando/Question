DNSWatch tracks malicious and suspicious domains; websites hosting phishing pages, distributing malware, command-and-control sites, and more. Lists of these domains are often shared on the internet. Let's write a program that allows us to search a list of "bad" domains for a specific domain. For example, "is google.com a bad domain?". Write the code so that it is easy for others to use and extend (as opposed to a one-time personal script). Consider:

- Performance.
- Readability.
- Extensibility.

### Part 1
Create a library to do the following:

- Maintain a list of "domain feed sources": URLs that contain some form of info about malicious domains.
- From each domain feed, fetch the data, parse it to collect domain names, and store them in an appropriate data structure.

It should support one domain feed:

- "MalwareDomains": http://mirror1.malwaredomains.com/files/justdomains

### Part 2
It should support an additional domain feed:

- "OpenPhish": https://openphish.com/feed.txt

Add a feature:

- Expose a search function which accepts a domain name argument, and returns which feeds (if any) the domain is present in.
