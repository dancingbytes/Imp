imp
======


Small daemons for ruby

### Supported environment

Ruby:   1.9.2, 1.9.3

Rails:  3.0, 3.1, 3.2


### Example

    require 'imp'    

    daemon = Imp.run( "name-of-your-proccess", File.join("Path", "to", "log.file") ) do

      # do some work

    end # Imp.run

    ["INT", "QUIT", "TERM", "KILL"].each do |signal|

      trap(signal) {
        daemon.stop
      }

    end # each


### License

Copyright (c) 2012 DansingBytes.ru

Author: Tyralion (piliaiev@gmail.com)

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.