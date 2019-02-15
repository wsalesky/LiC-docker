# LiC-docker
Docker image builder for the LiC software. Based on the eXist-db Docker image [https://hub.docker.com/r/existdb/existdb]. 

### This image pre-loads the following eXist-db libraries and modules: 
1. EXPATH Cryptographic Library Module v0.6 [http://exist-db.org/exist/apps/public-repo/packages/expath-crypto-exist-lib.html?eXist-db-min-version=4.4.0]
2. FunctX library [http://exist-db.org/exist/apps/public-repo/packages/functx.html]

### Additional Customizations
1. The image also includes a custom controller-config.xml and exist-webapp-context.xml to set the LiC app (/db/apps/LiC) as the root direcory, allowing users to access the application home page at http://localhost:8080/index.html. 
 
## How To Use
This repository uses GitHub submodules [https://git-scm.com/book/en/v2/Git-Tools-Submodules] to load the most recent version of the Srophe application and the Syriaca.org data. In order to build the application
and data packages you must explicitly pull the submodules when you clone the repository, and before rebuilding the image: 

```git submodule ini```

```git submodule update```

Or to update submodules: 

```git submodule foreach git pull origin master```
