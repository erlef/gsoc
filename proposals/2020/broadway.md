* Source code: https://github.com/dashbitco/broadway
* Ideas are listed in no particular order

### Idea #1: Fluentd input

The goal of this idea is to implement the endpoints necessary for an Elixir server to receive incoming messages from Fluentd instances. The protocol is called Fluentd Forward Protocol and is documented [here](https://github.com/fluent/fluentd/wiki/Forward-Protocol-Specification-v1).

For this task, the student will most likely use [ranch](https://github.com/ninenines/ranch/)/[cowboy](https://github.com/ninenines/cowboy/) to receive Fluentd requests. Direct integration with Broadway is not priority at the moment and should be tackled only if there is enough time.

**Expected results:** Be able to receive Fluentd events directly from Elixir

**Knowledge prerequisites:** Elixir

**Possible Mentors:** José Valim, Wojtek Mach, Marlus Saraiva

### Idea #2: Filebeat input

The goal of this idea is to implement the endpoints necessary for an Elixir server to receive incoming messages from filebeat. The protocol will be the same [Filebeat uses to communicate with Logstash](https://www.elastic.co/guide/en/beats/filebeat/current/logstash-output.html). Unfortunately, the protocol is not documented beyond [its reference implementations](https://discuss.elastic.co/t/beat-protocol/83295/2).

For this task, the student will most likely use [ranch](https://github.com/ninenines/ranch/)/[cowboy](https://github.com/ninenines/cowboy/) to receive Filebeat requests. Direct integration with Broadway is not priority at the moment and should be tackled only if there is enough time.

**Expected results:** Be able to receive Filebeat events directly from Elixir

**Knowledge prerequisites:** Elixir

**Possible Mentors:** José Valim, Wojtek Mach, Marlus Saraiva
