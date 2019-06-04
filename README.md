# Selenium Web Driver Installer  [![Build Status](https://travis-ci.com/shadowmoose/chrome_driver.svg?branch=master)](https://travis-ci.com/shadowmoose/chrome_driver)

This is a super-simple package that can automatically find & download the newest (or whichever you specify) version of 
the Google Chrome (chromedriver) or Firefox (geckodriver) web drivers.

This project was built to allow developers to seamlessly include selenium support on the user-side, without requiring any manual configuration on their part.

It is tested on Windows/Linx/Mac, and supports os-specific permissions.

To install the library, run:
```
pip install chromedriver-install
```


Then call it in your code like so:
```python
import chromedriver_install as cdi
path = cdi.install(browser=cdi.chrome, file_directory='./lib/', verbose=True, chmod=True, overwrite=False, version=None, filename=None, return_info=False)
print('Installed chromedriver to path: %s' % path)
```

There are options for the output directory, disabling printout, running chmod on the downloaded executable, 
automatic overwriting, executable file name, and version number. 
All parameters are optional, and the default values are listed above.

To download Firefox, simply change the `browser` parameter:
```python
import chromedriver_install as cdi
path = cdi.install(browser=cdi.firefox)
print('Installed geckodriver driver to path: %s' % path)
```
