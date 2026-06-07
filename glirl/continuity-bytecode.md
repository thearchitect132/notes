GLIRL Continuity Bytecode (v0.1)

Bytecode Format for the Continuity VM and Kernel Execution



1\. Purpose of Continuity Bytecode

Continuity Bytecode is the final compiled representation of continuity logic.



It is:



compact



deterministic



Pure‑NOT + PAIR only



metadata‑aware



VM‑executable



invariant‑bound



narrative‑aware



layer‑aware



It answers:



What is the exact binary‑level instruction format the Continuity VM executes?



Continuity Bytecode is the machine language of structural coherence.



2\. Bytecode Design Principles

Continuity Bytecode is designed to be:



minimal — only essential instructions



canonical — one encoding per logical meaning



deterministic — no nondeterminism allowed



traceable — metadata embedded



safe — invariant and layer checks enforced



optimisable — supports folding and caching



portable — same bytecode across arenas and layers



Bytecode is the lowest stable interface of continuity.



3\. Bytecode File Structure

A bytecode file consists of:



Code

HEADER

CONSTANT\_POOL

INSTRUCTION\_STREAM

METADATA\_TABLE

3.1 HEADER

Code

0x43 0x4F 0x4E 0x54   // "CONT"

version: u16

flags: u16

entry\_point: u32

Flags include:



LAYER\_AWARE



INVARIANT\_BOUND



NARRATIVE\_AWARE



DEBUG\_INFO



3.2 CONSTANT\_POOL

Constants include:



symbol references



literal TRUE/FALSE



invariant IDs



narrative tags



layer identifiers



Example:



Code

0x01: SYMBOL Apprentice

0x02: SYMBOL Builder

0x03: LITERAL TRUE

0x04: LITERAL FALSE

3.3 INSTRUCTION\_STREAM

A linear sequence of bytecode instructions.



3.4 METADATA\_TABLE

Maps instruction offsets to:



layer context



invariant context



narrative tags



lineage references



Metadata is execution‑critical.



4\. Bytecode Instruction Set

The Continuity VM executes a minimal instruction set.



4.1 Core Instructions

Mnemonic	Opcode	Args	Meaning

LOAD	0x01	const\_id	Push constant

NOT	0x02	—	Unary NOT

PAIR	0x03	—	Binary PAIR

PUSH	0x04	value	Push literal

POP	0x05	—	Pop stack

RET	0x06	—	Return result





These correspond directly to Pure‑NOT + PAIR.



4.2 Metadata Instructions

Mnemonic	Opcode	Args	Meaning

SET\_LAYER	0x10	layer\_id	Set active layer

SET\_INV	0x11	inv\_id	Bind invariant

SET\_NAR	0x12	tag\_id	Bind narrative tag

SET\_LIN	0x13	lineage\_id	Bind lineage





Metadata is enforced before execution of the next instruction.



4.3 Control Instructions

Mnemonic	Opcode	Args	Meaning

JUMP	0x20	offset	Unconditional jump

JUMP\_IF\_FALSE	0x21	offset	Conditional jump

HALT	0x22	—	Stop execution





Control flow is minimal but sufficient for composite continuity programs.



5\. Bytecode Encoding Examples

5.1 Example: NOT(Apprentice)

IR

Code

NOT(Apprentice)

Bytecode

Code

01 01      // LOAD Apprentice

02         // NOT

06         // RET

5.2 Example: PAIR(NOT(A), NOT(B))

IR

Code

PAIR(NOT(A), NOT(B))

Bytecode

Code

01 01      // LOAD A

02         // NOT

01 02      // LOAD B

02         // NOT

03         // PAIR

06         // RET

5.3 Example with Metadata

IR

Code

SET\_LAYER(Core)

NOT(PAIR(NOT(A), NOT(B)))

Bytecode

Code

10 00      // SET\_LAYER Core

01 01      // LOAD A

02         // NOT

01 02      // LOAD B

02         // NOT

03         // PAIR

02         // NOT

06         // RET

6\. Bytecode Validation Rules

The VM validates:



stack discipline



operand types



metadata consistency



invariant binding



narrative coherence



layer alignment



lineage correctness



Invalid Bytecode Examples

PAIR with <2 stack values



NOT with empty stack



undefined constant reference



missing metadata for invariant‑bound block



Validation ensures runtime safety.



7\. Bytecode Optimisations

The compiler and VM apply:



7.1 Constant Folding

Code

NOT TRUE → FALSE

7.2 Short‑Circuit PAIR

Code

PAIR(FALSE, x) → FALSE

7.3 Metadata Hoisting

Move metadata instructions earlier when safe.



7.4 Dead Code Elimination

Remove unreachable jumps.



7.5 Block Fusion

Merge adjacent blocks with compatible metadata.



8\. Bytecode and the Continuity VM

The VM executes bytecode by:



reading instruction



applying metadata



performing stack operation



checking invariants



checking narrative



checking layers



reducing truth value



Bytecode is the direct input to the VM.



9\. Bytecode and the Continuity Runtime

The Runtime uses bytecode for:



scheduling



memoisation



witness integration



state updates



graph updates



Bytecode is the runtime’s executable substrate.



10\. Summary

Continuity Bytecode:



is the lowest‑level representation of continuity logic



encodes Pure‑NOT + PAIR programs



embeds invariants, narrative, layers, and lineage



is executed deterministically by the Continuity VM



powers the Runtime, Engine, Simulator, and Dashboard



Continuity Bytecode =

the machine language of deep‑time coherence.

