# Private npm with docker

Slides in the slides folder (just open the index.html under `slides`)

Sample scripts in the root to start the relevant docker container.

There are two versions - `start-private-npm` stores the data on the host, and `start-private-npm-linked-data` uses data from a linked container (created with `create-npm-data-container`)

## Scripts
`start-private-npm` to start a private npm docker container (from [burkostya's image](https://github.com/burkostya/npm-registry/blob/master/Dockerfile)). Change the `/data/privatenpm` in the script to the direcctory where you want your npm (coucbdb) data to go, or use the other two other scripts to use a linked volume.  

`create-npm-data-container` creates a data volume container for use with `start-private-npm-linked-data`

`start-private-npm-linked-data` creates a docker container using the volumes from `create-npm-data-container`

