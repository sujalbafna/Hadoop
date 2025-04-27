**HDFS (Hadoop Distributed File System)**

**Definition:** HDFS (Hadoop Distributed File System) is the primary storage system of Hadoop. It is designed to store very large datasets reliably, and to stream those data sets at high bandwidth to user applications. HDFS stores data across multiple machines and provides fault tolerance by replicating data blocks across the cluster.

---

**HDFS Basic Commands with Example Outputs:**

1. **View Files in HDFS**

```bash
hdfs dfs -ls /
```

**Output:**

```
Found 3 items
drwxr-xr-x   - hadoop supergroup          0 2025-04-27 12:00 /input
drwxr-xr-x   - hadoop supergroup          0 2025-04-27 12:01 /output
drwxr-xr-x   - hadoop supergroup          0 2025-04-27 12:02 /user
```

2. **Create a Directory in HDFS**

```bash
hdfs dfs -mkdir /myfolder
```

**Output:**

```
(No output if successful)
```

3. **Copy a File from Local Filesystem to HDFS**

```bash
hdfs dfs -put /home/user/sample.txt /myfolder/
```

**Output:**

```
(No output if successful)
```

4. **Copy a File from HDFS to Local Filesystem**

```bash
hdfs dfs -get /myfolder/sample.txt /home/user/
```

**Output:**

```
(No output if successful)
```

5. **Display the Contents of a File**

```bash
hdfs dfs -cat /myfolder/sample.txt
```

**Output:**

```
Hello, this is a sample HDFS file.
```

6. **Remove a File from HDFS**

```bash
hdfs dfs -rm /myfolder/sample.txt
```

**Output:**

```
Deleted /myfolder/sample.txt
```

7. **Remove a Directory from HDFS**

```bash
hdfs dfs -rm -r /myfolder
```

**Output:**

```
Deleted /myfolder
```

8. **Move a File within HDFS**

```bash
hdfs dfs -mv /input/data.txt /output/
```

**Output:**

```
(No output if successful)
```

9. **Copy a File within HDFS**

```bash
hdfs dfs -cp /input/data.txt /output/data_copy.txt
```

**Output:**

```
(No output if successful)
```

10. **Check Disk Usage**

```bash
hdfs dfs -du /input
```

**Output:**

```
4096  /input/data.txt
```

11. **Show File Statistics**

```bash
hdfs dfs -stat %n %b %o /input/data.txt
```

**Output:**

```
data.txt 4096 16504150000
```

12. **List Directory Recursively**

```bash
hdfs dfs -ls -R /
```

**Output:**

```
-rw-r--r--   1 hadoop supergroup  4096 2025-04-27 12:00 /input/data.txt
-rw-r--r--   1 hadoop supergroup  4096 2025-04-27 12:00 /output/data_copy.txt
```

13. **Change File Permissions**

```bash
hdfs dfs -chmod 755 /input/data.txt
```

**Output:**

```
(No output if successful)
```

14. **Change File Ownership**

```bash
hdfs dfs -chown user1:group1 /input/data.txt
```

**Output:**

```
(No output if successful)
```

15. **Show File Content in Human-readable Format**

```bash
hdfs dfs -text /input/data.txt
```

**Output:**

```
Hello, this is a sample HDFS file.
```
