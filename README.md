### About Me

Chemical Engineer (**BSc, Budapest University of Technology and Economics — BME**) transitioning into **Software Engineering** (**CTeSP TPSI at ISPGAYA**, Porto), combining a quantitative foundation in mathematical modeling and process simulation with clean software architecture.

Focused on backend development in **C# (.NET 8)**, low-level systems programming in **C11**, algorithmic modeling in **Python**, and relational databases.

- **Portfolio:** [yancsalmeida.github.io](https://yancsalmeida.github.io/)
- **Curriculum Vitae:** [English (PDF)](https://yancsalmeida.github.io/cv/CV_Yan_Almeida_Software_Engineer_EN.pdf) · [Português (PDF)](https://yancsalmeida.github.io/cv/CV_Yan_Almeida_Software_Engineer_PT.pdf)
- **LinkedIn:** [linkedin.com/in/yancsa](https://www.linkedin.com/in/yancsa/)

---

### Selected Projects

- **[`IndustrialTelemetry.Engine`](https://github.com/yancsalmeida/IndustrialTelemetry.Engine)** (`C# 12 · .NET 8 · PostgreSQL 16 · Clean Architecture · Docker`) — Asynchronous telemetry ingestion pipeline and batch execution state machine. Uses bounded in-memory channels (`System.Threading.Channels`) with a background consumer worker for micro-batch flushing and direct PostgreSQL Binary `COPY` (`NpgsqlBinaryImporter`) on composite time-series indexes `(batch_id, timestamp_utc)`. Enforces strict batch lifecycle transitions (`Scheduled` → `InProgress` → `Completed`/`Aborted`) with compliance auditing and real-time threshold alarms.
- **[`ChemFlow.NET`](https://github.com/yancsalmeida/ChemFlow.NET)** (`C# 12 · .NET 8 · Clean Architecture · SignalR · C11 P/Invoke · SQLite`) — Modular steady-state process and thermodynamic simulation engine. Implements the Peng-Robinson cubic equation of state (analytical Cardano solver), safeguarded Newton-Raphson Rachford-Rice flash calculations, and a staged multicomponent distillation column (MESH solver via Thomas Algorithm / TDMA and Holland's $\theta$-method). Resolves directed acyclic flowsheets with recycles using Kahn's topological sort and Wegstein acceleration, integrating native C11 ODE solvers via P/Invoke and streaming simulation state over ASP.NET Core SignalR.
- **[`ProcessTwin.Py`](https://github.com/yancsalmeida/ProcessTwin.Py)** (`Python 3.12 · FastAPI · Asyncio · ctypes FFI · WebSockets`) — Real-time industrial process Digital Twin and supervisory telemetry service. Bridges Python asynchronous loops to compiled C11 (`libreactorcore.so`) via `ctypes` FFI (9.4x batch speedup with IEEE-754 parity), emulates 4–20 mA transmitter noise, evaluates automated safety interlocks (IEC 61511 SIS logic), and broadcasts 5 Hz state updates over WebSockets.
- **[`ReactorCore.C`](https://github.com/yancsalmeida/ReactorCore.C)** (`C11 · GCC · Shared C-ABI · Makefile`) — Zero-dependency C11 dynamic chemical reactor solver. Integrates coupled non-linear mass and energy ordinary differential equations (Arrhenius kinetics and jacket heat transfer) via classical 4th-order Runge-Kutta (RK4) function pointers, pre-allocating contiguous workspace memory to eliminate heap allocations inside numerical loops and exposing a shared C-ABI (`reactor_ffi.h`).
- **[`cs-fundamentals`](https://github.com/yancsalmeida/cs-fundamentals)** (`C11 · C# / .NET 8 · Python 3 · Linux x86_64`) — Systems programming and concurrency laboratories covering Linux `x86_64` virtual memory layouts, pointer arithmetic, thread synchronization primitives, and discrete time-series filtering.

---

### Technical Stack

- **Languages:** `C# (.NET 8)`, `C (C11)`, `Python 3 (Asyncio)`, `SQL`, `Bash`
- **Backend & Data:** `ASP.NET Core Web API`, `Entity Framework Core`, `Dapper`, `Npgsql` (Binary `COPY`), `System.Threading.Channels`, `SignalR`, `FastAPI`, `PostgreSQL 16`, `SQLite`
- **Systems & Architecture:** Clean Architecture, Native C-ABI / FFI (`P/Invoke`, `ctypes`), Directed Acyclic Graphs (Topological Sort), Numerical Solvers (RK4, Newton-Raphson, TDMA), Low-Level Memory Management
- **Environment & Tooling:** Linux (Ubuntu), Docker & Docker Compose, Git, GitHub Actions (CI), `xUnit`, `pytest`
