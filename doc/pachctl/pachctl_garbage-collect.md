## ./pachctl garbage-collect

Garbage collect unused data.

### Synopsis


Garbage collect unused data.

When a file/commit/repo is deleted, the data is not immediately removed from the underlying storage system (e.g. S3) for performance and architectural reasons.  This is similar to how when you delete a file on your computer, the file is not necessarily wiped from disk immediately.

To actually remove the data, you will need to manually invoke garbage collection.  The easiest way to do it is through "pachctl garbage-collect".

Currently "pachctl garbage-collect" can only be started when there are no active jobs running.  You also need to ensure that there's no ongoing "put-file".  Garbage collection puts the cluster into a readonly mode where no new jobs can be created and no data can be added.


```
./pachctl garbage-collect
```

### Options inherited from parent commands

```
      --no-metrics   Don't report user metrics for this command
  -v, --verbose      Output verbose logs
```

### SEE ALSO
* [./pachctl](./pachctl.md)	 - 

###### Auto generated by spf13/cobra on 2-Aug-2018
