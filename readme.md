@echo off

set SCRIPT_PATH=%cd%

cd %SCRIPT_PATH%

echo Press [CTRL+C] to stop mining.

:begin

 for /f %%i in ('coincli.exe getnewaddress') do set WALLET_ADDRESS=%%i
 
 coin-cli.exe generatetoaddress 1 %WALLET_ADDRESS%
 
goto begin




2 option bat

@echo off

set path_cli=%cd%

cd %path_cli%

echo Press [CTRL+C] to stop mining.

:begin

coin-cli.exe generate 1

goto begin