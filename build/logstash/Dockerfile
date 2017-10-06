FROM logstash:5

ENV LOGSTASH_PLUGINS="logstash-codec-oldlogstashjson logstash-input-eventlog logstash-input-log4j logstash-input-zeromq logstash-filter-anonymize logstash-filter-checksum logstash-filter-multiline logstash-output-email logstash-output-exec logstash-output-gelf logstash-output-juggernaut logstash-output-lumberjack logstash-output-zeromq"
# NOT INSTALLED: logstash-output-nagios_nsca logstash-output-opentsdb logstash-output-ganglia logstash-output-hipchat

RUN for plugin in $LOGSTASH_PLUGINS; do /usr/share/logstash/bin/logstash-plugin install $plugin; done
