https://roadmap.sh/projects/nginx-log-analyser

# Solution :

IP Address Count :
`awk '{print $1}' nginx.log | sort | uniq -c | sort -nr | head -n 5 | awk '{print $2 " - " $1 " requests"}' > ip-most-requested.log`

Link Count :
`awk '{print $7}' nginx.log | sort | uniq -c | sort -nr | head -n 5 | awk '{print $2 " - " $1 " requests"}' > link-most-requested.log`

Status Code Count :
`awk '{print $9}' nginx.log | sort | uniq -c | sort -nr | head -n 5 | awk '{print $2 " - " $1 " requests"}' > most-status-code-requested.log`
