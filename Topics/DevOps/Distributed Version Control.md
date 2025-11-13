___
***Distributed version control*** is a form of version control in which the complete codebase, including its full history, is mirrored on every developer's computer.
___
Distributed version control systems take a peer-to-peer approach, as opposed to the client–server approach of centralized systems. Rather than a single, central repository on which clients synchronize, each peer's working copy of the codebase is a repository. Distributed version control conducts synchronization by exchanging patches (commits) from peer to peer. 

This results in some important differences from a centralized system:
- No canonical, reference copy of the codebase exists by default, only working copies.
- Common operations (such as commits, viewing history, and reverting changes) are fast, because there is no need to communicate with a central server.
- Communication is only necessary when pushing or pulling changes to or from other peers.
- Each working copy effectively functions as a remote backup of the codebase and of its change-history, providing inherent protection against data loss.

This arrangement can be difficult to maintain, resulting in many projects choosing to shift to a paradigm in which one contributor is the universal "upstream", a repository from whom changes are almost always pulled. Under this paradigm, development is somewhat recentralized, as every project now has a central repository that is informally considered as the official repository, managed by the project maintainers collectively.

While distributed version control systems make it easy for new developers to "clone" a copy of any other contributor's repository, in a central model, new developers always clone the central repository to create identical local copies of the code base. Under this system, code changes in the central repository are periodically synchronized with the local repository, and once the development is done, the change should be integrated into the central repository as soon as possible.

Organizations utilizing this centralize pattern often choose to host the central repository on a third party service, which offers not only more reliable uptime than self-hosted repositories, but can also add centralized features like issue tracking and continuous integration.