#!/usr/bin/python

import re
import os
import sys
debug = True

lines = sys.stdin.readlines()
lemma = sys.argv[1]

# INPUT:
# - lines contain a list of "%i:goal" where "%i" is the index of the goal
# - lemma contain the name of the lemma under scrutiny
# OUTPUT:
# - (on stdout) a list of ordered index separated by EOL


rank = []             # list of list of goals, main list is ordered by priority
maxPrio = 110
for i in range(0,maxPrio):
  rank.append([])

#, multp\(H_n_2.*P1.*, multp\(~f,.*~TPM_EK_Seed


if lemma[0:7]=="correct":
  print ("applying oracle to "+lemma)
  for line in lines:
    num = line.split(':')[0]
    if re.match('.*KU\(~.*', line): rank[109].append(num)
    elif re.match('.*KU\( senc.*', line): rank[108].append(num)
    elif re.match('.*KU\( p.*', line): rank[107].append(num)


else:
    print ("not applying the rule")
    exit(0)

# Ordering all goals by ranking (higher first)
for listGoals in reversed(rank):
  for goal in listGoals:
    sys.stderr.write(goal)
    print (goal)
