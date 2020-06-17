# PyAudio for PyPy3
`pypy3 -m pip install pyaudio` fails to install PyAudio for PyPy3. This is because PyPy3 C-API is slightly different from CPython C-API.

Install PortAudio from source: http://www.portaudio.com/download.html
```bash
cd
wget http://portaudio.com/archives/pa_stable_v190600_20161030.tgz
tar -zxvf pa_stable_v190600_20161030.tgz
cd portaudio
./configure && make
sudo make install
```

Install PyAudio for PyPy3:
```bash
git clone https://github.com/iovsiann/pyaudio
cd pyaudio
pypy3 -m pip install .
```

# Original PyAudio
Original source code at http://people.csail.mit.edu/hubert/pyaudio/

```
======================================================================
PyAudio v0.2.8: Python Bindings for PortAudio.
======================================================================

See: http://people.csail.mit.edu/hubert/pyaudio/

PyAudio provides Python bindings for PortAudio v19, the cross-platform
audio I/O library. Using PyAudio, you can easily use Python to play
and record audio on a variety of platforms.

See INSTALL for compilation hints.

======================================================================

PyAudio : Python Bindings for PortAudio.

Copyright (c) 2006-2014 Hubert Pham

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

======================================================================
```
