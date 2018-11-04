### go script for uploading lambda functions to aws

### Build
```
 go build
 ```
### Run the program with flags: 
``` 
-c - path to json project.json configuration file
-n - name of the functions
-d - golang user folder (if case it is different than default)
example: go-aws -c ../big-project/functions/project.json -n func1
```

### Key information
1. You must have configured aws (region, credentials)
2. You must have created aws s3 bucket and role
3. project.json and the function have to be in the same folder
4. project.json must contain keys: 'Name', 'Bucket', 'Role', i.e. :
``` 
{
  "Name": "myname",
  "Bucket": "mybucket",
  "Role": "myrole"
}
```
