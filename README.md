Kafka Producer for the PAS network
==================================================
This program is connecting to the PAS Ntrip Caster (as the Ntrip Client) mountpint (this is defined as the -d argument). After it gets the streaming data from the caster, it will decode the data into the RINEX3 format and put the RINEX3 data into the Kafka queue (as the kafka producer).

the example command:


./rdkafka_simple_producer -s [NtripCasterURL] -r [Port] -u [Username] -p [Password] -b [KafkaBrokers] -M 1 -d [Mountpoint] -3 -k [KafkaTopic]

for example:

./rdkafka_simple_producer -s test2.test.com -r 1234 -u test262 -p ppppqqqqq -M 1 -d 12345678903 -3 -k mytopic -b localhost:9092

## Build from source

./configure

make
