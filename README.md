# nextgenconnect

A quick little NextGen Connect client for testing

## Get it running

```
docker-compose up -d
open mirthconnect.jnlp
```

- Username: **admin**
- Password: **admin**

_TIP: get past Welcome dialog quickly by entering admin for username, new password, & confirm password, then unchecking register option to be able to click Finish button_

## Set up a TCP channel

1. In left gutter, click on **Channels** > **New Channel**
2. Enter "**test**" as channel name
3. Click on **Source tab** and set connector type to **TCP**
4. In left gutter, click on **Deploy Channel**, clicking yes to save changes as you deploy

## Monitor for message

Under **Dashboard** (from left gutter), double click on your test channel to see channel messages.

## Send a test message

```
groovy TestMllp.groovy
```

or if you don't have Groovy installed, using Docker:

```
docker run --rm -v $PWD/TestMllp.groovy:/TestMllp.groovy --network host groovy \
  groovy /TestMllp.groovy
```
