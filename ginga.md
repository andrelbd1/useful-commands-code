### [Ginga](http://www.ginga.org.br/) commands

#### Install on Ubuntu
````bash
    sudo add-apt-repository ppa:telemidia/daily-builds
    sudo apt-get update
    sudo apt-get install ginga-itv
````

#### Compile
````bash
    ./bootstrap
    ./configure
    make
    sudo make install
````

#### Compile and enable warnings by maint.mk
````bash
    ./bootstrap
    ./configure --enable-warnings
    make
````

#### Show configure options
````bash
    ./bootstrap
    ./configure --help
````

#### Compile and enable debug options
````bash
    ./bootstrap
    ./configure --enable-debug
    make
````

#### Compile and enable GDB
````bash
    ./bootstrap
    ./configure --enable-debug --disable-shared
    make
````

#### Compile and check tests
````bash
    ./bootstrap
    ./configure
    make check
````

#### Compile to check a especific test
````bash
    ./bootstrap
    ./configure
    make check TESTS='tes-Event-transition-Media-PAUSE'
````

#### Checking log tests
````bash
    cat tests/test-Event-transition-Media-PAUSE.log
````

#### Script to enable environment variables to make tests
````bash
    source tests/env.sh
````

#### Checking tests coverage
````bash
    ./bootstrap
    ./configure --enable-coverage
    make clean
    make -j9 coverage
````

#### Generating Doxygen documentation
````bash
    ./bootstrap
    ./configure
    make doc
````
