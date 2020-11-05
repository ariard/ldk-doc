# ldk-doc

This documentation is a work-in-progress, mostly the collection of past discussions with developers,
rather than a well-structured documentation.

## Getting Started

LN is a powerful protocol and LDK a flexible platform, before to get started on hacking, you may
be willingly to laid out those questions to design better your application.

1. Do you want your service to be custodial/non-custodial ? Beyond key management, bear in mind,
that a non-custodial service must also provide redundant chain watching to the client, otherwise
your service is "trusted" to watch the chain and punish rightfully your counterparty.
2. What privacy do you want to provide ? If payment-path construction is delegated to a service, 
the user loses recipient anonymity on its payments.
3. What level of fault-tolerance ? Your user may lose its key material and channel state, redundant
backups isn't a luxury.
4. What channel & liquidity UX ? A service may be delegated with liquidiy management and thus responsible
of channel rebalancing operations.
5. What payment UX ? Actually both parties have to be online to receive a payment, some [solutions](
https://medium.com/breez-technology/introducing-lightning-rod-2e0a40d3e44a) are worked out by the community
6. Do you want to provide cheap payments between service users ? By opening a channel to the node
service, cheap payments are available among the same users of the service
7. Do you want your users to have a network-wise identifier ? A LN public-key or a token issued from
it might serve as an authentication for some LN services
8. What resources do you expect from your users ? Bandwidth, disk, liveness, LN knowledge, fees costs, ...

