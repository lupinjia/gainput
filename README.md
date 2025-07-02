[Gainput](https://github.com/jkuhlmann/gainput)
=======

Gainput is the awesome C++ input library for your game:

- handles your input needs from low-level device reading to high-level mapping of user-defined buttons
- well-documented, clean, lightweight, and easy to use
- a unified interface on all supported platforms: **Android NDK, iOS/tvOS, Linux, macOS, Windows**
- supported devices: keyboard, mouse, gamepad, multi-touch, device built-in sensors
- [Open Source (MIT license)](https://github.com/jkuhlmann/gainput/blob/master/LICENSE)
- [complete list of features](#features)
- [API documentation](http://gainput.johanneskuhlmann.de/api/)

## Added features

- cmake find package support
	
	After `cmake ..`, `make`, `make install`, you will find libraries under `/usr/local/lib/gainput`, header files under `/usr/local/include`, then you can add following sentences to your CMakeLists.txt to use gainput:

	```cmake
	find_package(gainput REQUIRED)
	set(GAINPUT_LIBRARIES "gainput" "X11" "GL" "rt" CACHE PATH "Gainput library directory")
	include_directories(
    ${GAINPUT_INCLUDE_DIRS})
	link_directories(
    /usr/local/lib/gainput # add gainput library path
	)
	target_link_libraries(target
    ${GAINPUT_LIBRARIES}
  )
	```