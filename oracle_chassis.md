# Oracle Chassis

- Cannot access remote console due to certification issue
  - Enable SSLv3 by removing xxx.disableAlgorithm = SSLv3 in $JAVA_HOME/jre/lib/security/java.security
- Enable Oracle CMM Java Console Redirection with Java 1.8
  - Turn off your firewall
  - Find and run javacpl.exe, add the http address AND http address with port used by blade
  - Make sure that $JAVA_HOME/lib/security/java.security has not disabled SSLv3 (safest to comment out all disabledAlgorithms)
  - Add the URLs of the iLO web pages (WITH PORTS) to the list of certificate exceptions on your Google Chrome browser