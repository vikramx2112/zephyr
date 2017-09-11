:orphan:

.. _zephyr_1.9:

Zephyr Kernel 1.9.0 (WIP)
#########################

We are pleased to announce the release of Zephyr kernel version 1.9.0
(planned for release in August 2017).

Major enhancements planned with this release include:

* Pthreads compatible API
* BSD Sockets compatible API
* Expand Device Tree support to more architectures
* BLE Mesh
* Bluetooth 5.0 Support (all features except Advertising Extensions)
* Expand LLVM Support to more architectures
* Revamp Testsuite, Increase Coverage
* Zephyr SDK NG
* Eco System: Tracing, debugging support through 3rd party tools
* Lightweight Machine to Machine (LwM2M) support

These enhancements are planned, but may move out to a future release:

* Thread Protocol (initial drop)
* MMU/MPU (Cont.): Thread Isolation, Paging
* Build and Configuration System (CMake)


The following sections provide detailed lists of changes by component.

Kernel
******

* change description

Architectures
*************

* arm: Added STM32F405, STM32F417, STM32F103x8 SoCs
* arm: Added TI CC2650 SoC
* arm: Removed TI CC3200 SoC
* arm: Added MPU support to nRF52, STM32L4, and STM32F3
* xtensa: Added ESP32

Boards
******

* Added device tree support for Intel Quark based microcontroller boards
  such as Arduino_101, tinytile, and Quark_d2000_crb.
* arm: Added Atmel SAM4S Xplained board
* arm: Added Olimex STM32-E407 and STM32-P405 boards
* arm: Added STM32F412 Nucleo and STM32F429I-DISC1 boards
* arm: Added TI SensorTag board
* arm: Removed TI CC3200 LaunchXL board
* arm: Added VBLUno51 and VBLUno52 boards
* xtensa: Added ESP32

Drivers and Sensors
*******************

* KW40Z IEEE 802.15.4 radio driver support added
* APDS9960 sensor driver added
* Added TICKLESS KERNEL support for nrf RTC Timer
* Added Kinetis adc and pwm drivers
* Removed deprecated PWM driver APIs
* Added ESP32 drivers for GPIO, pin mux, watchdog, random number generator,
  and UART

Networking
**********

* LWM2M support added
* net-app API support added. This is higher level API that can be used
  by applications to create client/server applications with transparent
  TLS (for TCP) or DTLS (for UDP) support.
* MQTT TLS support added
* Add support to automatically setup IEEE 802.15.4 and Bluetooth IPSP networks
* TCP receive window support added
* Network sample application configuration file unification, where most of the
  similar configuration files were merged together
* Added Bluetooth support to HTTP(S) server sample application
* BSD Socket compatible API layer, allowing to write and/or port simple
  networking applications using a well-known, cross-platform API
* Networking API documentation fixes
* Network shell enhancements
* Trickle algorithm fixes
* Improvements to HTTP server and client libraries
* CoAP API fixes
* IPv6 fixes
* RPL fixes

Bluetooth
*********

* Bluetooth Mesh support (all mandatory features and most optional ones)
* GATT Service Changed Characteristic support
* IPSP net-app support: a simplified networking API reducing duplication
  of common tasks an application writer has to go through to connect
  to the network.
* BLE controller qualification-ready, with all required tests passing
* Controller-based privacy (including all optional features)
* Extended Scanner Filter Policies support in the controller
* Controller roles (Advertiser, Scanner, Master and Slave) separation in
  source code, conditionally includable
* Flash access cooperation with BLE radio activity

Build and Infrastructure
************************

* change description

Libraries
*********

* mbedTLS updated to 2.6.0
* TinyCrypt updated to 0.2.7

HALs
****

* change description

Documentation
*************

* CONTRIBUTING.rst and Contribution Guide material added
* Configuration options doc reorganized for easier access
* Navigation sidebar issues fixed for supported boards section
* Completed migration of wiki.zephyrproject.org content into docs and
  GitHub wiki. All links to old wiki updated.
* Broken link and spelling check scans through .rst, Kconfig (used for
  auto-generated configuration docs), and source code doxygen comments
  (used for API documentation).
* API documentation added for new interfaces and improved for existing
  ones.
* Documentation added for new boards supported with this release.
* Python packages needed for document generation added to new python
  pip requirements.txt


Tests and Samples
*****************

* Added test Case to stress test round robin scheduling in schedule_api test.
* Added test case to stress test priority scheduling in scheduling_api_test.


JIRA Related Items
******************

.. comment  List derived from Jira query: ...

* :jira:`ZEP-000` - Title
