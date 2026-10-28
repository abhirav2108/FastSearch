# FastSearch (C++ Multithreaded Log Analyzer)

A high-performance, concurrent file-searching utility built in standard C++. FastSearch dispatches multiple threads to scan massive log files simultaneously, drastically reducing search times compared to sequential processing.

## Core Architecture
* **Concurrency:** Utilizes `std::thread` to spawn independent worker threads for each target file.
* **Thread Safety:** Implements `std::mutex` and `std::lock_guard` to prevent race conditions during standard output (I/O) operations, ensuring clean and accurate console reporting.
* **Resource Management:** Ensures safe thread joining and lifecycle management to prevent memory leaks and zombie threads.

## Technologies Used
* **Language:** Standard C++ (C++11 and later)
* **Libraries:** `<thread>`, `<mutex>`, `<fstream>`, `<vector>`

## Usage
Compile the source code using any standard C++ compiler (GCC/MinGW/MSVC):
`g++ fastsearch.cpp -o fastsearch.exe`

Execute the binary:
`.\fastsearch.exe`
