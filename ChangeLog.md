### wolfSSH v1.4.3 (10/31/2019)

- wolfSFTP port to MQX 4.2 (MQX/MFS/RTCS)
- Maintenance and bug fixes
- Improvements and additions to the test cases
- Fix some portablility between C compilers
- Fixed an issue in the echoserver example where it would error sometimes
  on shutdown
- Improvement to the global request processing
- Fixed bug in the new keys message handler where it reported the wrong size
  in the data buffer; invalid value was logged, not used
- Fixed bug in AES initialization that depended on build settings
- Improved interoperability with puTTY
- Added user auth callback error code for too many password failures
- Improvements to the Nucleus filesystem abstraction
- Added example for an "autopilot" file get and file put with the wolfSFTP
  example client


### wolfSSH v1.4.2 (08/06/2019)

- GCC 8 build warning fixes
- Fix for warning with enums used with SFTP and set socket type
- Added example server with Renesas CS+ port
- Fix for initializing UserAuthData to all zeros before use
- Fix for SFTP “LS” operation when setting the default window size to 2048
- Add structure size print out option -z to example client when the macro
  WOLFSSH_SHOW_SIZES is defined
- Additional automated tests of wolfSSH_CTX_UsePrivateKey_buffer and fix for
  call when key is already loaded
- Refactoring done to internal handling of packet assembly
- Add client side public key authentication support
- Support added for global requests
- Fix for NULL dereference warning, rPad/sPad initialization and SFTP check on
  want read. Thanks to GitHub user LinuxJedi for the reports
- Addition of WS_USER_AUTH_E error returned when user authentication callback
  returns WOLFSSH_USERAUTH_REJECTED
- Remove void cast on variable not compiled in with single threaded builds


### wolfSSH v1.4.0 (04/30/2019)

- SFTP support for time attributes
- TCP port forwarding feature added (--enable-fwd)
- Example tcp port forwarding added to /examples/portfwd/portfwd
- Fixes to SCP, including default direction set
- Fix to match ID during KEX init
- Add check for window adjustment packets when sending large transfers
- Fixes and maintenance to Nucleus port for file closing
- Add enable all option (--enable-all)
- Fix for --disable-inline build
- Fixes for GCC-7 warnings when falling through switch statements
- Additional sanity checks added from fuzz testing
- Refactor and fixes for use with non blocking
- Add extended data read for piping stderr
- Add client side pseudo terminal connection with ./examples/client/client -t
- Add some basic Windows terminal conversions with wolfSSH_ConvertConsole
- Add wolfSSH_stream_peek function to peek at incoming SSH data
- Change name of internal function SendBuffered() to avoid clash with wolfSSL
- Add support for SFTP on Windows
- Use int types for arguments in examples to fix Raspberry Pi build
- Fix for fail case with leading 0’s on MPINT
- Default window size (DEFAULT_WINDOW_SZ) lowered from ~ 1 MB to ~ 16 KB
- Disable examples option added to configure (--disable-examples)
- Callback function and example use added for checking public key sent
- AES CTR cipher support added
- Fix for free’ing ECC caches with examples
- Renamed example SFTP to be examples/sftpclient/wolfsftp


### wolfSSH v1.3.0 (08/15/2018)

- Accepted code submission from Stephen Casner for SCP support. Thanks Stephen!
- Added SCP server support.
- Added SFTP client and server support.
- Updated the autoconf scripts.
- Other bug fixes and enhancements.

### wolfSSH v1.2.0 (09/26/2017)

- Added ECDH Group Exchange with SHA2 hashing and curves nistp256,
  nistp384, and nistp521.
- Added ECDSA with SHA2 hashing and curves nistp256, nistp384, and nistp521.
- Added client support.
- Added an example client that talks to the echoserver.
- Changed the echoserver to allow only one connection, but multiple
  connections are allowed with a command line option.
- Added option to echoserver to offer an ECC public key.
- Added a Visual Studio solution to build the library, examples, and tests.
- Other bug fixes and enhancements.

### wolfSSH v1.1.0 (06/16/2017)

- Added DH Group Exchange with SHA-256 hashing to the key exchange.
- Removed the canned banner and provided a function to set a banner string.
  If no sting is provided, no banner is sent.
- Expanded the make checking to include an API test.
- Added a function that returns session statistics.
- When connecting to the echoserver, hitting Ctrl-E will give you some
  session statistics.
- Parse and reply to the Global Request message.
- Fixed a bug with client initiated rekeying.
- Fixed a bug with the GetString function.
- Other small bug fixes and enhancements.

### wolfSSH v1.0.0 (10/24/2016)

Initial release.
