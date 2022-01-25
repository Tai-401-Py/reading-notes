
# reflection and discussion 03
---

## Revisions and the Cloud
---

### Version control
---

What is version control, well it's a catalogue of revisions made. So you can go back and look at what was done. 

- Local Version control
  - Revisions stored on a local database (hard drive) for easy recall
  - Allows for singular control of revisions
- Centralized Version Control
  - Revisions stored on a central database such as a server for easy access by numerous parties
  - Allows for numerous people to work together
- Distributed Version Control
  - Uses mirrored(duplicated) repositories to store revisions, to be merged at a later date
  - Allows many teams to work in tandem
  - Prvents data loss by having multiple copies of full revision history across multiple devices
  
### Git
---

Git is a DCVS (Distributed Version Control System) that stores revisions in snapshots.

- Snapshot
  - Each time you commit (make revisions) to a file Git creates a snapshot (copy) of the version and adds it to the repository (file storage) 
- Local operations
  - Project history resides on local hard drive eliminating the need to get data from server. Allowing you to work offline.
- Revision Tracking
  - Git tracks changes made to every file and directory and acts as a gate keeper to prevent file loss or corruption during transit.
- Loss of Data
  - Git makes it difficult to lose all revisions of a file once they are commited. Allowing you to recover lost work easily. (assuming it's been commited)
- States
  - Files can reside in one of three states on Git
    - Commited
      - Data Stored in local database
    - Modified
      - File data jhas been changed but not commited to database
    - Staged
      - File's changed version ready to be commited in next snapshot 

Setting up
1. Change to target directory
2. Use `git init` command to start git
3. To start tracking use the following
  - `git add *.c`
  - `git add LICENSE`
  - `git commit -m "any message here"`
 
Cloning
-Copying an existing repository
