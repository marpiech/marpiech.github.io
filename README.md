## Contents
### Gists
#### Admin
[Add user](#adduser)  
[Set .htpasswd](#htpasswd)
#### AWS
[Delete all log streams for log group](#delete-all-log-streams-for-log-group)


## Gists
<a name="adduser"></a>
#### Add user
[gist](https://gist.github.com/marpiech/1c601a1595324e10393a0fc56635ef5d)
```
#gitlab
curl https://gist.githubusercontent.com/marpiech/1c601a1595324e10393a0fc56635ef5d/raw/9b291f62888266fbbf4ddb0c0710ad0c1097df18/adduser.sh | bash /dev/stdin [username] [gitlab username]
#github
https://gist.githubusercontent.com/marpiech/1c601a1595324e10393a0fc56635ef5d/raw/6c06ed9a3af5d0b5565192f98a1db96bebdf3917/adduser.sh | bash /dev/stdin [username] [github username]
```

<a name="htpasswd"></a>
#### Set .htpasswd
```
sudo htpasswd -c /etc/apache2/.htpasswd marpiech
```

#### Delete all log streams for log group
```
aws logs describe-log-streams --log-group-name "/aws/batch/job" | jq ".logStreams[].logStreamName" | xargs -i bash -c "echo {}; aws logs delete-log-stream --log-group-name /aws/batch/job --log-stream-name {}"
```
