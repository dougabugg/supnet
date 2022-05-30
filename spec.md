# Specification

Just spitballing some ideas right now.

## Glossary

- `endpoint`: is defined as a tunnel or pipe thru which messages can be sent to and received from.
- `message`: can be of many different types; a stream of bytes, a fixed-sized payload, and optional
requirements for latency, TTL, bandwidth, priority, urgency, delivery confirmation, etc.

in the "backend", multi-homing is used to guarantee delivery requirements of messages, as needed.
for example, if a message is urgent or high priority, it will be sent via multiple IP network routes;
for a routine background sync of data, a low bandwidth but unmetered IP connection will be preferred, etc.

some amount of encryption will be baked into the protocol too, and might be configurable (to reduce latency, for example)
