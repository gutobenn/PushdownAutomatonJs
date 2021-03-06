PushdownAutomatonJs
===================

A generic deterministic pushdown automaton simulator in javascript.
Also supports multiple stacks (turing complete), a single stack (context-free languages) and no stack (finite automaton).

The machine definition used is as followed:<br>
`M = {Σ, Q, Π, q0, F, V}`<br>
Where:<br>
`M` := Machine<br>
`Σ` := Alphabet<br>
`Q` := States set<br>
`Π` := Program function<br>
`q0` := Initial state (`q0 ∈ Q`)<br>
`F` := Final states<br>
`V` := Auxiliary alphabet

The program function for a machine with n stacks is as folow:<br>
  `Π(cq, rq, rs1, ..., rsn) = (nq, ws1, ..., wsn)`

Where:<br>
  `cq` := Current state<br>
  `rq` := symbol read from the queue<br>
  `rsi` := symbol read (popped) from the ith stack<br>
  `nq` := Next state<br>
  `wsi` := symbol written (pushed) to the ith stack
