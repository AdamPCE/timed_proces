##########################################################################
# Description
#    o     Runs a command, and terminates it (by sending a signal) after
#     a specified time period
#    o     This command first starts itself as a "watchdog" process in the
#     background, and then runs the specified command.
#     If the command did not terminate after the specified
#     number of seconds, the "watchdog" process will terminate
#     the command by sending a signal.
#
# Notes
#    o     Uses the internal command line argument "-p" to specify the
#     PID of the process to terminate after the timeout to the
#     "watchdog" process.
#    o     The "watchdog" process is invoked by the name "$0", so
#     "$0" must be a valid path to the script.
#    o     If this script runs in the environment of the login shell
#     (i.e. it was invoked using ". timeout command...") it will
#     terminate the login session.
##########################################################################
