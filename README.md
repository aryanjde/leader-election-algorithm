# CS324 Assignment 1 — Distributed Worker System

<<<<<<< Updated upstream
## Package structure
- `com.cs324.common` — shared RMI interfaces (`WorkerRemote`, `BootstrapRemote`) and `Constants`
- `com.cs324.bootstrap` — Bootstrap Node (worker registry only, no election/job role)
- `com.cs324.worker` — Worker nodes (election, coordination, job execution)
- `com.cs324.client` — Client GUI (job submission)

## Requirements
- JDK 24
- Maven (or use NetBeans/VS Code's built-in Maven support)

## Build
```
mvn compile
```

## Run (once implemented)
Start each component in its own terminal, from the project root:

1. Bootstrap Node:
   ```
   mvn exec:java -Dexec.mainClass=com.cs324.bootstrap.BootstrapNode
   ```
2. Worker Node(s) — repeat with different IDs/ports for each worker:
   ```
   mvn exec:java -Dexec.mainClass=com.cs324.worker.WorkerNode -Dexec.args="<id> <port>"
   ```
3. Client(s):
   ```
   mvn exec:java -Dexec.mainClass=com.cs324.client.ClientApp
   ```

## Status
Project skeleton only — `common` interfaces and placeholder classes are in place.
Implementation (election logic, job splitting, GUI) is in progress.

## Team
- Shamal Prasad — S11219545
- Ravinesh Narayan — S11197324
- Isaiah Narayan — S11175115
=======
## First-Time Setup

**1. Clone the repo**
```
git clone <your-repo-URL>
cd A1_CS324
```

**2. Switch to your branch**
```
git checkout aryan
```
(or `suri` / `alvin`)

If the branch isn't showing up locally:
```
git fetch origin
git checkout -b aryan origin/aryan
```

**3. Build the project**
```
mvn compile
```

---

## Every Time You Work On This

**1. Pull the latest changes first**
```
git pull origin aryan
```

**2. Run the system**

Bootstrap Node (start first, one only):
```
mvn exec:java -Dexec.mainClass=com.cs324.bootstrap.BootstrapNode -Dexec.args="1099"
```

Worker Node (one per terminal, unique id + port each time):
```
mvn exec:java -Dexec.mainClass=com.cs324.worker.WorkerNode -Dexec.args="5 3500 localhost 1099"
```

Client (Swing GUI):
```
mvn exec:java -Dexec.mainClass=com.cs324.client.ClientApp
```

**3. Push your changes when done**
```
git add -A
git commit -m "your message here"
git push origin aryan
```

---

## Packages
- `common` — shared RMI interfaces + constants
- `bootstrap` — Bootstrap Node
- `worker` — Worker nodes (election + job execution)
- `client` — Client GUI
```
>>>>>>> Stashed changes
