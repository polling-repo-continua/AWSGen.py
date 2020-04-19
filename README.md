### AWS S3 Bucket Name Generator (beta v.)
---

__AWSGen.py__ is a simple tool for generates permutations, alterations and mutations of AWS S3 Buckets Names

Example:

![example](https://raw.githubusercontent.com/m4ll0k/AWSGen.py/master/example.png)


example:

```shell

$ for i in $(python3 awsgen.py www.dev-aws.example.com)
do
  code=$(curl -i -s $i -I|grep -i 'http'|awk '{print $2}')
  if [[ $code == 200 || $code == 403 ]]
  then
    echo "[$code] $i"
  fi
done

```
