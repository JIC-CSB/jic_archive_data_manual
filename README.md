# JIC guide to archiving data

## Identify data to archive

Data from historical group members and published papers are good starting points.


## Clean up your data

Remove any unnecessary files.


## Structure your data

Create a directory for your project.

```
mkdir my_project
```

Create a ``README.yml`` file in the top level.
Create a directory named ``archive`` in your project directory.

```
mkdir my_project/archive
```

Move all your data into the ``archive`` directory.


## Run the manifest generation script

```
python generate_manifest.py my_project/archive
```


## Zip the data

```
tar -zcvf my_project.tar.gz my_project
```


## Copy the data on the sync server

Log into the sync server and copy the data to your archive.


## Verify the transfer

On the archive system extract the README and manifest files.

```
tar -zxvf my_project.tar.gz my_project/README.yml
tar -zxvf my_project.tar.gz my_project/manifest.json
```
