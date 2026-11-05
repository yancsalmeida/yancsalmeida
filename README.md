### About Me

Chemical Engineer transitioning into **Software Engineering**, combining a strong foundation in mathematical modeling and process simulation with clean software architecture.

Focused on backend development in **C# / .NET**, low-level systems programming in **C**, algorithmic modeling in **Python**, and relational databases.

---

### Featured Projects

- **[`IndustrialTelemetry.Engine`](https://github.com/yancsalmeida/IndustrialTelemetry.Engine)** — Enterprise manufacturing telemetry ingestion, batch process execution state machine, and real-time safety alarm engine built with **C# 12 / .NET 8**, **Clean Architecture**, and **PostgreSQL 16**. Features a high-throughput ingestion pipeline with an asynchronous bounded in-memory channel (`System.Threading.Channels`), hosted background consumer worker (`BackgroundService`) with micro-batch flushing, direct zero-allocation PostgreSQL Binary `COPY` (`NpgsqlBinaryImporter`), composite time-series indexing `(batch_id, timestamp_utc)`, automated safety rule evaluation (`TT-101`, `PT-101`, `pH-101`, `RPM-101`), strict batch lifecycle state transitions (`Scheduled` → `InProgress` → `Completed`/`Aborted` with compliance auditing), live queue status inspection (`/api/telemetry/channel/status`), **Docker Compose**, and **xUnit** test suites (41 automated tests).
- **[`ChemFlow.NET`](https://github.com/yancsalmeida/ChemFlow.NET)** — Modular steady-state chemical process and thermodynamic simulation engine built with **C# 12 / .NET 8** and **Clean Architecture**. Features advanced equation-of-state thermodynamics with the **Peng-Robinson Cubic Equation of State (PR-EOS)**, Cardano analytical cubic root solver, van der Waals mixing rules with binary interaction parameters ($k_{ij}$), fugacity coefficients, enthalpy departure functions, Antoine vapor pressure correlations, safeguarded Newton-Raphson **Rachford-Rice** isothermal flash solver, unit operations (`Mixer`, `HeaterCooler`, `FlashDrum`, `ConversionReactor`, `ContinuousStirredTankReactor`), native **C11 P/Invoke** integration with **`ReactorCore.C`** (`libreactorcore.so`) for continuous dynamic reaction ODE integration, **Kahn's topological sort** for DAG flowsheet execution, Graphviz/DOT process flow diagram (PFD) topology export, plant-wide mass and energy balance closure validation ($\Delta m / m < 10^{-5}$, $\Delta H / H < 10^{-4}$), **ASP.NET Core** endpoints, **SQLite (`ADO.NET`)** persistence with schema migration, interactive Web Studio dashboard, and automated **`xUnit`** test suites (42 tests).
- **[`ProcessTwin.Py`](https://github.com/yancsalmeida/ProcessTwin.Py)** — Real-time industrial process Digital Twin and SCADA telemetry engine built with **Python 3.12**, **FastAPI**, **Asyncio**, **Pydantic v2**, and **aiosqlite**. Integrates directly with native **C11 (`ReactorCore.C`)** via a high-performance **`ctypes` FFI bridge** (`libreactorcore.so`), achieving a **9.4x batch integration speedup** (2.66M steps/s) with zero bit-level IEEE-754 discrepancy. Emulates sensor noise ($\mathcal{N}(0, \sigma^2)$) on 4–20 mA transmitters, evaluates **Safety Instrumented System (SIS / IEC 61511)** emergency interlocks, streams 5 Hz live telemetry over **WebSockets**, connects to **`ChemFlow.NET`** via an asynchronous client bridge for real-fluid Peng-Robinson cubic thermodynamics, auto-negotiates batches and streams telemetry into `IndustrialTelemetry.Engine`, and features an interactive dark-mode SCADA dashboard with SVG instrumentation and Canvas strip charts (48 automated tests).
- **[`ReactorCore.C`](https://github.com/yancsalmeida/ReactorCore.C)** — High-performance continuous chemical reactor dynamic simulation engine and ODE solver built in **C11 (`gcc`)** with zero external dependencies. Features cache-friendly workspace pre-allocation (zero heap allocation in numerical loops), classical **4th-Order Runge-Kutta (RK4)** integration via **C function pointers**, non-linear **Arrhenius** reaction kinetics, jacket heat-transfer dynamics, thermal runaway detection, exported C ABI (`include/reactor_ffi.h`, `libreactorcore.so`) for native multi-language FFI interop, and automated unit tests verifying $O(\Delta t^4)$ convergence (27 tests in C).
- **[`cs-fundamentals`](https://github.com/yancsalmeida/cs-fundamentals)** — Systems programming and algorithmic modeling laboratories in **C# (.NET 8)**, **C11 (`gcc`)**, and **Python 3** on Linux `x86_64`, covering virtual memory layouts, pointer arithmetic, concurrency primitives, and discrete process telemetry analysis.

---

### Technical Stack

- **Languages:** `C# (.NET 8)`, `C (C11)`, `Python 3 (Asyncio)`, `SQL`, `Bash`
- **Backend, Data & Ingestion:** `ASP.NET Core Web APIs`, `Entity Framework Core`, `Npgsql`, PostgreSQL Binary `COPY`, `System.Threading.Channels`, `FastAPI`, Clean Architecture, `ADO.NET` / `aiosqlite` / `SQLite`, WebSockets, `xUnit`, `pytest`, OpenAPI / Swagger
- **Computer Science & Interop:** Native C ABI / FFI (`ctypes`, C# P/Invoke / `NativeLibrary`), Algorithms & Data Structures (Graphs, Topological Sort, Numerical ODE Solvers), Asynchronous Event-Driven Systems, Low-Level Memory Management
- **Environment & Tooling:** Linux (Ubuntu), Docker & Docker Compose, Git & GitHub, GitHub Actions (CI), `uv`

---

## Author

**Yan Almeida**
- LinkedIn: [linkedin.com/in/yancsa](https://www.linkedin.com/in/yancsa/)
- GitHub: [github.com/yancsalmeida](https://github.com/yancsalmeida)
