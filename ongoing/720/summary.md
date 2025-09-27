---
title: "JavaScript Blazingly FAST! Lessons from a Game Engine - Erik Onarheim - NDC Oslo 2025 (en)"
date: 2025-09-28T00:11:00.467+02:00
category: videos
tags: [JavaScript, performance optimization, web development, web workers, WebAssembly, debugging, memory management, JIT compiler, profiling, game development]
excerpt: "Comprehensive guide to making JavaScript fast: understanding JIT, memory, workers, optimization strategies, WebAssembly, and profiling tools."
---

![thumbnail](https://i.ytimg.com/vi/xCB9cB9YZL8/maxresdefault.jpg)
[https://youtu.be/xCB9cB9YZL8?si=mndfY9B_pb057WGx](https://youtu.be/xCB9cB9YZL8?si=mndfY9B_pb057WGx)

<!--- My thoughts -->

## Content

### Why JavaScript and the Importance of Performance
Eric discusses why JavaScript remains essential despite not being the fastest language. Given that JavaScript runs everywhere—including websites and critical real-time apps like games, chat applications, and simulations—making it performant matters. Slow JavaScript can cost businesses real revenue and impact user experience via CPU, battery usage, and responsiveness. 

He stresses that while performance optimization can improve speed, it often reduces maintainability and increases bugs, so developers should carefully evaluate if faster code is worth the complexity. Setting clear, measurable performance goals is crucial.

> “Performance optimization often makes code harder to read and have insidious bugs. So, you need to think about: is this even worth doing?”

### How JavaScript Works: Interpreter to JIT
JavaScript engines load scripts from the network, parse them into bytecode via interpreters, and optimize hot code paths with Just-In-Time (JIT) compilers which generate machine code dynamically. Understanding this pipeline helps target optimization strategies.

### Tools for Profiling and Debugging
Chrome and Firefox DevTools provide powerful tools for profiling CPU usage, memory usage, and tracking calls with flame charts and hot path detection. Node.js debugging can also use Chrome's DevTools. These tools are essential for measuring before and after optimization.

### Big-Effort Gains: Cheating and Multi-threading
Appearing fast is sometimes enough; UI tricks like spinners and animation can improve perceived performance. Then, to utilize multiple cores, web workers allow multi-threading in JavaScript, but developers must be aware of data copying costs with postMessage and prefer transferables like ArrayBuffer for large datasets.

### Data Structures and Loop Optimizations
Using the right data structures such as Maps, Sets, WeakMaps, Heaps, and implementing caching (memoization) can drastically reduce computation time. Loop performance can be improved by:
- Hoisting invariants out of loops
- Using C-style for loops instead of functional methods like forEach or map
- Writing cache-coherent loops accessing contiguous memory to exploit CPU cache lines.

### Data-Oriented Programming
Organizing data in bulk (such as entity component systems in game development) helps the CPU process data without unpredictable branches, improving branch prediction and cache utilization. Avoid branching conditions inside loops by segregating data by state.

### Coroutines for Smooth Performance
Co-routines using JavaScript generators allow spreading expensive computations over multiple frames to avoid blocking the main thread, useful for animations or incremental work.

### Leveraging WebAssembly
WebAssembly (Wasm) provides a high-performance, secure, sandboxed execution environment with consistent performance and SIMD (vectorized operations). It supports many languages, allows reuse of existing libraries, and can outperform Node.js's native FFI calls in many cases. However, large binary sizes and debugging complexity are downsides. Wasm excels in compute-heavy applications like video encoding and image processing (e.g., Google's Squoosh). 

### GPU for Parallel Tasks
GPUs excel at highly parallel, math-heavy problems such as particle simulations, fluid dynamics, neural networks, and computer vision but are not suited for logic-heavy code with branching. WebGPU is an upcoming standard but not yet widely usable.

### Memory Management and Avoiding Leaks
JavaScript uses generational garbage collection. Memory leaks can arise from unintentional global variables, lingering event handlers, forgotten timers, closures holding large references, detached DOM nodes, and debug console logs holding references. Tools like heap snapshots and performance monitors help identify leaks.

Memory thrashing from frequent allocations causes jank and minor GC pauses. Mitigate this with pre-allocated scratch variables and object pools or arenas which recycle objects instead of creating new ones continuously.

### Maximizing JIT Performance
The JIT compiler creates optimized machine code based on runtime types and hidden classes. Programming practices to maintain monomorphic code include consistently constructing objects with the same property order and avoiding adding properties at runtime. Deoptimizations cause slowdowns but can re-optimize as code warms up.

### Preventing Regression and Maintaining Performance
Run benchmark tests regularly, ideally on a consistent hardware setup, to track performance changes. Continuous measurement and focusing on largest bottlenecks prevents wasted effort and maintains stability.

### Final Recommendations
Set measurable goals, focus on big optimizations first, and apply scientific methods through measurement and iteration. Eric recommends resources such as Front-End Masters courses and talks by V8 engineers to deepen understanding.

> "Set a goal and apply science. Don’t just keep digging because you can."

This comprehensive walkthrough equips developers with practical strategies and nuanced understanding to optimize JavaScript performance in real-world applications.
