# Bandit Level 10

In this level the password is stored in the file `data.txt`, which contains base64 encoded data.

When we view the contents of the file we are greeted with this:

![b612b8db.png](../src/b612b8db.png)

Because this data is encoded as base64, we need to decode it. This can be done with `base64`. To decode data the flag `-d` is used
> `base64 -d data.txt`

This reveals the password: `IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR`
