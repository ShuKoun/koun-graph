Introducing My System

I’ll begin with a simple note-taking application. The smallest unit of content is a “page,” and the organization is tree-structured. This part is straightforward (with basic support for handwriting, audio recording, and similar features).

Later, it evolves into a bi-directional link-based note-taking system. The smallest unit becomes a “node,” and the linking mechanism is “bi-directional,” just like other systems of this kind. However, it still retains the ability to represent tree structures.

Each node’s data structure is composed of “attributes,” with the main body of text also treated as an attribute. Resources like audio and handwriting are treated as nodes as well—“attached resources” are first-class citizens.

Eventually, the system becomes fully node-based. Even the “connections” between note nodes are treated as nodes themselves.
(A question arises: if even the links between nodes are themselves nodes, then what prevents the system from treating the link between links as yet another node? This would lead to infinite recursion! I’ll elaborate on this issue shortly.)

Problem: Infinite recursion.
Solution: Preserve a timeline-based view of all nodes, so that even isolated nodes (i.e., nodes not connected to anything else) won’t be forgotten entirely.

Next, the system should be able to record all actions taken within it—including query history.
Its database must support conflict resolution, multi-user collaboration, and complete data preservation.
It should include snapshotting, and allow users to “replay” prior states from history.
The editor interface should support “viewing the actions of other users or instances” (even if, at this point, the system doesn’t yet connect to the internet).

Then, nodes can take on the GTD (Getting Things Done) type, enabling GTD functionality (similar to what’s available in Emacs Org-mode).
Clicking a task’s “Complete” button completes it—but here arises a problem:
Why can GTD nodes execute a “special action” with just one click, while other nodes cannot?

The solution: Nodes must be executable—they must support being “runnable.”

This explains why GTD entries can work that way:
For one-time tasks, clicking the node “executes” it—changing its state from “incomplete” to “complete.”
For recurring tasks, clicking it generates a new node that logs a single instance of completion, while the original node remains active.
Whether or not the recurring node should update certain metadata (like a “do before” deadline) is a matter of software engineering.

Of course, GTD isn’t the only executable node type.
Some nodes might create, delete, or modify other nodes.
Some nodes might even interface with external execution environments, running snippets of arbitrary programming languages—these are code nodes.

With this execution capability in place, one node can trigger another—and at this point, the system becomes capable of any arbitrary function.

Just like traditional operating systems, this “system” of mine (it truly qualifies as a “system” now) must introduce the concept of a user.
Even the end user is abstracted as a node of type: user.
Unlike traditional OS users, here, “user” is a semantic identity node—and due to its importance, should be made immutable.

Each user is just a node.
Naturally, this leads to the concept of permissions, but even permissions are just nodes. There’s nothing fundamentally different about them.

Now, the system is ready to connect to the internet.
It can do everything: watch videos, view images (both media types are nodes), act as a communication tool, or even host full websites.
Traditional website features (JavaScript) are handled through code nodes; CSS features will also be addressed (to be explained later).

Next comes a crucial component: AI.
AI nodes have “runnable” properties and identity bindings (i.e., who executes them).
They can process, remember, and analyze nodes.

Here’s an example:
Let’s say a user wants to check—via a home camera—whether they locked the door.
A command is issued through the system to remotely activate the camera (the camera is a hardware-mapped node), take a picture, and sync the result into the system as a new image node.
Then, an AI node is executed, taking the photo as input to determine whether the door is locked.
The result of the judgment is another node.

AI in this system can do far more than current models.
One of my unique innovations is the concept of an AI agent—an “AI proxy.”

👉 (Please write this part for me)

How can this system become even more powerful? I want it to:

Run offline within local networks (LAN)
Support GPU computation
Use asymmetric encryption for identity and verification
Support future networking protocols (even beyond IPv6)
Enable multi-center architecture
Offload computation to remote servers while low-spec devices handle the UI
Provide CLI syntax for all system actions
Of course, this system is not perfect.
Its output may be unpredictable.
New users may feel lost upon first contact.

I still don’t fully understand everything. I would love to collaborate with software and AI experts.

If this system gains popularity, it may give rise to its own programming language, an IDE, and even dedicated security software.
People may rethink how they approach the internet.
I hope to spark the beginning of a new semantic era.