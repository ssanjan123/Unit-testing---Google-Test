# Unit Testing with Google Test and GMock

<img src="https://user-images.githubusercontent.com/84153519/213343493-141648ee-dd5e-45e4-ae7f-b54108c87424.png" width="500" height="500">


## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

- C++ compiler (e.g. g++)
- Google Test and GMock libraries (if the provided libraries are not compatible with your system)

### Installing

1. Clone the repository
git clone https://github.com/yourusername/unit-testing-google-test-gmock.git

Copy code

2. Install Google Test and GMock libraries
    - On Ubuntu:
    ```
    sudo apt-get install libgtest-dev
    ```
    ```
    sudo apt-get install libgmock-dev
    ```
    - On MacOS: 
    ```
    brew install gtest
    ```
    ```
    brew install gmock
    ```
3. Build the libraries 
    ```
    cd /usr/src/gtest
    ```
    ```
    sudo cmake CMakeLists.txt
    ```
    ```
    sudo make
    ```
    ```
    sudo cp *.a /usr/lib
    ```
    ```
    cd /usr/src/gmock
    ```
    ```
    sudo cmake CMakeLists.txt
    ```
    ```
    sudo make
    ```
    ```
    sudo cp *.a /usr/lib
    ```

### Running the tests

1. Navigate to the project directory
cd unit-testing-google-test-gmock

Copy code

2. Compile the test files
g++ -std=c++11 -pthread -I/usr/include/gmock -I/usr/include/gtest -c test_files.cpp

Copy code
3. Link the test files 
g++ -std=c++11 -pthread -L/usr/lib -lgtest -lgtest_main -lgmock -lgmock_main test_files.o -o test_files

Copy code
4. Run the test files 
./test_files

Copy code

## Built With

* [C++](https://en.wikipedia.org/wiki/C%2B%2B) - The programming language used
* [Google Test](https://github.com/google/googletest) - The testing framework used
* [GMock](https://github.com/google/googletest/tree/master/googlemock) - The library used for creating test doubles (e.g. mocks, stubs)
