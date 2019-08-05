Kafka Producer for the PAS network
==================================================
This program is connecting to the PAS Ntrip Caster (as the Ntrip Client) mountpint (this is defined as the -d argument). After it gets the streaming data from the caster, it will decode the data into the RINEX3 format and put the RINEX3 data into the Kafka queue (as the kafka producer).

the example command:
./rdkafka_simple_producer -s [NtripCasterURL] -r [Port] -u [Username] -p [Password] -b [KafkaBrokers] -M 1 -d [Mountpoint] -3

# Installation

## Installing prebuilt packages

On Mac OSX, install librdkafka with homebrew:

```bash
$ brew install librdkafka
```

On Debian and Ubuntu, install librdkafka from the Confluent APT repositories,
see instructions [here](https://docs.confluent.io/current/installation/installing_cp/deb-ubuntu.html#get-the-software) and then install librdkafka:

 ```bash
 $ apt install librdkafka-dev
 ```

On RedHat, CentOS, Fedora, install librdkafka from the Confluent YUM repositories,
instructions [here](https://docs.confluent.io/current/installation/installing_cp/rhel-centos.html#get-the-software) and then install librdkafka:

```bash
$ yum install librdkafka-devel
```

On Windows, reference [librdkafka.redist](https://www.nuget.org/packages/librdkafka.redist/) NuGet package in your Visual Studio project.


For other platforms, follow the source building instructions below.


## Build from source

### Requirements
	The GNU toolchain
	GNU make
   	pthreads
	zlib-dev (optional, for gzip compression support)
	libssl-dev (optional, for SSL and SASL SCRAM support)
	libsasl2-dev (optional, for SASL GSSAPI support)
	libzstd-dev (optional, for ZStd compression support)

