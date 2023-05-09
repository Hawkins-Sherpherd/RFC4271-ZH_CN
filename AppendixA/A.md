Comparison with RFC 1771

   There are numerous editorial changes in comparison to [RFC1771] (too
   many to list here).

   The following list the technical changes:

      Changes to reflect the usage of features such as TCP MD5
      [RFC2385], BGP Route Reflectors [RFC2796], BGP Confederations
      [RFC3065], and BGP Route Refresh [RFC2918].

      Clarification of the use of the BGP Identifier in the AGGREGATOR
      attribute.

      Procedures for imposing an upper bound on the number of prefixes
      that a BGP speaker would accept from a peer.

      The ability of a BGP speaker to include more than one instance of
      its own AS in the AS_PATH attribute for the purpose of inter-AS
      traffic engineering.

      Clarification of the various types of NEXT_HOPs.

      Clarification of the use of the ATOMIC_AGGREGATE attribute.

      The relationship between the immediate next hop, and the next hop
      as specified in the NEXT_HOP path attribute.

      Clarification of the tie-breaking procedures.

      Clarification of the frequency of route advertisements.

      Optional Parameter Type 1 (Authentication Information) has been
      deprecated.

      UPDATE Message Error subcode 7 (AS Routing Loop) has been
      deprecated.

      OPEN Message Error subcode 5 (Authentication Failure) has been
      deprecated.

      Use of the Marker field for authentication has been deprecated.

      Implementations MUST support TCP MD5 [RFC2385] for authentication.

      Clarification of BGP FSM.