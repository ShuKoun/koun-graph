# 1. My System: Evolution from Note-Taking to a Semantic Operating System

## 1.1 Starting Point: Page-Based Tree Note System

I began with a simple note-taking application.  
The smallest unit was a "page," and the overall structure was tree-based.  
This stage was intuitive and supported basic features like handwriting and audio recording.

## 1.2 Bidirectional Linking and Node System

Next, the system evolved into a note-taking model with bidirectional linking.  
At this point, the smallest unit was no longer a page, but a "node"; the linking mechanism was bidirectional, similar to systems like Obsidian.  
Tree-style visualization was still preserved.

Each node had an attribute-based data structure, with the main body of text also treated as an attribute.  
Audio, handwriting, and other resources were also treated as nodes—"attached resources" became first-class citizens.

## 1.3 Fully Node-Based System: Even Relationships Become Nodes

Eventually, I transitioned the system to a fully node-based model. Even the connections between note nodes became nodes themselves.

This raised a philosophical and implementation challenge:

> If connections are nodes, can you then point to a connection?  
> And then point to the pointer of a connection?  
> Would this lead to infinite recursion?

Here I propose a solution:

✅ Introduce a "Semantic Convergence" mechanism. When potential recursive structures emerge, the system doesn’t block such links, but allows the semantic graph to evolve and **converge naturally** based on structural tension and semantic consensus, rather than collapse or explode.

Details of this mechanism are discussed later in the **Semantic Convergence** section.

Simultaneously, I assign every node a timestamp index. Even if a node becomes disconnected, it remains retrievable through the timeline to prevent semantic isolation.

## 1.4 Behavior Logging and Query History

The next step was to enable recording of all actions, including query history.

Thus, the database must:
- Support conflict resolution;
- Enable multi-user collaboration;
- Preserve all states without overwriting;
- Support snapshots and replay of history;
- Allow users to view actions of other users or instances—even offline.

## 1.5 Task Nodes × GTD × Executable Nodes

I wanted nodes to support GTD (Getting Things Done) behaviors, similar to Emacs Org-mode.

For example, clicking a “Complete” button on a task node marks it as done.

This raised a question:

> Why can only GTD nodes trigger special behavior? Why not other nodes?

### 1.5.1 Solution: Executability

All nodes should be executable. That is, each node should have a `runnable` property.

### 1.5.2 Node = Function × State Transition

- One-time task: clicking changes the node’s state from "incomplete" to "complete".
- Recurring task: clicking generates a new node to record that instance of completion, while the original node stays active.

Whether to update metadata (like `do-before`) is a software engineering detail.

## 1.6 Node Triggering × Structure as Logic

- Some nodes create other nodes;
- Some delete or modify nodes;
- Some interact with external execution environments, running code snippets. These are "code nodes."

Once nodes can trigger each other, the system becomes Turing-complete.

## 1.7 User Node × Semantic Identity × Immutability

Users are also nodes—type: `user`. They are **semantic identity nodes** and should be immutable.

This leads to:
- Permission nodes;
- User relationship nodes;
- Construction of identity networks.

## 1.8 Networking × Media Nodes × Site Hosting

The system can now:
- Play videos (video = node);
- Display images (image = node);
- Serve as a communication tool;
- Host full websites;
- Replace JavaScript with code nodes; CSS node modeling is in development.

## 1.9 AI Nodes × Structural Interaction × Judgement Generation

AI nodes have:
- Executability;
- Identity binding;
- The ability to receive inputs, produce outputs, and modify other nodes.

### 1.9.1 Example

> “Did I lock the door?” → Trigger camera (hardware node) → take picture → image becomes node → AI node analyzes → result returned as new node.

## 1.10 AI Proxy: An Introduction 🧠

AI is no longer just a model, but a **semantic agent (AI Proxy)**.

These nodes:
- Perceive graph structures;
- Track memory chains;
- Initiate perspectives and semantic tension;
- Simulate reasoning and collaborate with other agents.

📚 For more, see my paper: *Semantic Agents: Reconstructing AI as Structural Participants.*

## 1.11 Semantic Convergence

To address semantic divergence from excessive versions, I introduce **Semantic Convergence**:

- Structural weighting;
- Inference centroids;
- Consensus graph modeling;
- Multi-agent fusion between human and AI perspectives.

📚 For details, see: *Semantic Consensus: Convergence in Tension Fields.*

## 1.12 Vision and Reflection

Planned capabilities:
- Offline LAN support;
- GPU inference support;
- Asymmetric encryption for identity;
- Protocol abstraction beyond IP;
- Multi-center architecture;
- Lightweight frontend + remote computation;
- Full CLI support for all node actions.

## 1.13 Final Thoughts: A Syntax for the Semantic Universe

This system is not yet perfect:
- Outcomes may be unpredictable;
- Beginners may feel lost;
- Even I have not fully grasped its boundaries.

But I hope it may one day:
- Evolve its own language and IDE;
- Spawn new security and interop protocols;
- Redefine how we perceive "networks," "operating systems," and "intelligence";
- And become a structural grammar for a new semantic civilization.

Please view my paper [KounGraph: A Semantic Node-Based Operating System and Its Cognitive Structure Model](https://doi.org/10.5281/zenodo.15244182)