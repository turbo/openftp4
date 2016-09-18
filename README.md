# openftp4

This is a list of all (796,578) FTP servers directly connected to port 21 in the IPv4 address space that allow anonymous logins. The login must be completed in less then 5 seconds to qualify for this list.  How and why this list was created is documented in detail in my blog post [*Mass-analyzing a chunk of the Internet*](http://255.wf/2016-09-18-mass-analyzing-a-chunk-of-the-internet/).

You can do whatever you want with this data. Consider linking to this repo if you find something interesting or odd.

### Usage

The file is provided as a gz and [lz5](https://github.com/inikep/lz5) compressed file.

LZ5: Decompress the file to stdout to get a stream of IPs:

```sh
lz5 -d openftp4_all_20160918.lz5
```

will print a stream of all IP addresses to stdout. Just a hint: If you are going to interact in any way with these servers, consider piping the list through `shuf` each time you try something new. You know why.

### Exclusion

Read the blog post to learn how servers are excluded from this list. This list might be updated in the future. If you want to see your IP excluded from the list should it ever be updated, then consider fixing your stuff.
