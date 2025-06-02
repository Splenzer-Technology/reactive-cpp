# Reactive C++

Reactive C++ is a lightweight, high-performance UI framework that brings React-like declarative syntax to C++ using an XML-based domain-specific language (.cpx). It compiles directly to native C++ for optimal speed, with zero runtime overhead.

## ✨ Features

- ✅ React-style declarative UI in `.cpx`
- ⚡ Compiles to fast native C++ (no virtual machine)
- 🪟 GLFW + NanoVG (planned) for cross-platform rendering
- 🛠 TinyXML2-based transpiler
- 🧩 Extensible component model
- 🌐 Open-source and community-driven

---

## 📦 Folder Structure

reactive-cpp/
├── transpiler/ # Parses .cpx and generates .cpp
│ └── main.cpp
├── runtime/ # C++ UI runtime components
│ ├── UI.h
│ └── UI.cpp
├── examples/ # Example .cpx source + generated .cpp
│ ├── hello.cpx
│ └── hello.cpp
├── CMakeLists.txt
└── README.md

---

## 🚀 Quick Start

1. Clone the repo:

```bash
git clone https://github.com/yourname/reactive-cpp.git
cd reactive-cpp

1. Build the project:

mkdir build && cd build
cmake ..
make


3. Run the transpiler on an example:
./transpiler/transpiler ../examples/hello.cpx ../examples/hello.cpp


4. Compile the generated C++ 
g++ ../examples/hello.cpp ../runtime/UI.cpp -o hello -lglfw -ldl -lGL
./hello


Sample .cpx UI
<Window title="Demo" width="800" height="600">
  <VStack>
    <Text>Welcome</Text>
    <Button onClick="handleClick">Click Me</Button>
  </VStack>
</Window>



