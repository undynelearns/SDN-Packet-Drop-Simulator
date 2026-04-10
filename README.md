# SDN Packet Drop Simulator using Mininet

## Problem Statement
Simulate packet loss using SDN flow rules in Mininet and analyze network behavior.

##Setup
- Mininet installed on Ubuntu VM
  
2. Start Mininet:
   sudo mn --topo single,3 --controller=remote

3. Test connectivity:
   pingall

4. Apply drop rule:
   ovs-ofctl add-flow s1 priority=100,ip,nw_src=10.0.0.1,nw_dst=10.0.0.2,actions=drop

5. Test:
   h1 ping h2 (fails)
   h1 ping h3 (works)

## Results
- Selective packet drop achieved
- Flow rules control traffic behavior

## Regression Test
After restart, flow rules are cleared.

## Proof
Screenshots included
