# openftp4

This is a list of all (796,578) FTP servers directly connected to port 21 in the IPv4 address space that allow anonymous logins. The login must be completed in less than 5 seconds to qualify for this list.  How and why this list was created is documented in detail in my blog post [*Mass-analyzing a chunk of the Internet*](http://255.wf/2016-09-18-mass-analyzing-a-chunk-of-the-internet/).

You can do whatever you want with this data. Consider linking to this repo if you find something interesting or odd.

### Usage

The file is provided as a gz and [lz5](https://github.com/inikep/lz5) compressed file.

LZ5: Decompress the file to stdout to get a stream of IPs:

```sh
lz5 -d openftp4_all_20160918.lz5
```

will print a stream of all IP addresses to stdout. Just a hint: If you are going to interact in any way with these servers, consider piping the list through `shuf` each time you try something new so you don't hit the same server(s) over and over again. Also, don't sort the list before rescanning, because you will enounter IP slashes that belong to one network. Think about what it looks like from their perspective ;-).

If you want to be extra nice, provide your actual email address (or one you have access to) as the password (blog post for details), so server admins can contact you. 

## [![](https://news.ycombinator.com/y18.gif) Discussion](https://news.ycombinator.com/item?id=12523455)

- News: [SoftPedia](http://news.softpedia.com/news/nearly-800-000-ftp-servers-accessible-online-without-authentication-508421.shtml) &#8226; [D. Pratt (German)](https://dominicpratt.de/unsichere-ftp-server/)
- Discussion elsewehre: [HN](https://news.ycombinator.com/item?id=12527989) &#8226; [r/DataHoarder](https://www.reddit.com/r/DataHoarder/comments/53cyhm/list_of_all_anonymous_login_ftp_servers_worldwide/) &#8226; [r/opendirectories](https://www.reddit.com/r/opendirectories/comments/53b0ar/a_list_of_all_ftp_servers_in_the_whole_internet/) &#8226; [r/netsec](https://www.reddit.com/r/netsec/comments/53bori/massanalyzing_a_chunk_of_the_internet/) &#8226; [r/sysadmin](https://www.reddit.com/r/sysadmin/comments/53cor1/someone_just_posted_every_open_ftp_server_on_ipv4/) 

### In the Wild

Applications that use this dataset:

- http://exploreftp.host (seems to struggle a bit atm): Explore a random FTP server.

### Exclusion

(This doesn't concern FTP servers that are public by design.)

Read the blog post to learn how servers are excluded from this list. This list might be updated in the future. If you want to see your IP excluded from the list should it ever be updated, then consider fixing your stuff.
