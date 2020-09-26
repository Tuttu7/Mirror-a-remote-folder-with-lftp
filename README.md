
### How to mirror a remote folder with lftp


```
lftp sftp://user:password@server.org:22 -e 'mirror --verbose --use-pget-n=8 -c /remote/path /local/path'
```
* sftp:// = uses SFTP protocol
* mirror = mirror mode
* verbose = shows the files being downloaded
* use-pget-n = number of segments, realy useful to speed up big files
* parallel = downloads multiplier files at the same time
* If you want to download files in parallel switch out use-pget-n=8 with --parallel=8
