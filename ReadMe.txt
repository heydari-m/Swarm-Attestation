The Tamarin codes for Swarm attestation protocol were added.
These files are related to different phases of the protocol including setup, registration, attestation and report phases.

For att.spthy please:

First check/change the permission of the Oracle.py to 755
chmod 755 Oracle.py

and then execute:

tamarin-prover interactive . --heuristic=O --oraclename=Oracle.py

in the directory where your att.spthy and Oracle.py are stored
