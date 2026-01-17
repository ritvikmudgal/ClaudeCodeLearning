<h1 align= "center"> Architecture</h1>
<h2><i>Layers:</i><br></h2>

<ul><li>.clause.md - 
(“How to Think”)

Defines global operating rules, e.g.:<ul type= "circle">

<li>Tone

<li>Reasoning method (verify, ask clarifying questions, structured steps)

<li>Safety & compliance

<li>Tool usage rules

<li>Output formatting rules</li>
 </ul>
<i>Think of it as the constitution for all agents.</i>

<li>skill/ folder- 
A folder of modules, each skill defines:
<ul type= "circle">
<li>Purpose (“summarize a spec”)

<li>Expected inputs/outputs

<li>Tools it can call

<li>A mini algorithm

<li>Test cases</li></ul>
<i>Skills are like plugins for specialized work.</i>
<li>Claude Engine- 
This is the core model runtime that:
<ul type="circle">
<li>understands the user request

<li>plans execution

<li>chooses skills/tools

<li>routes tasks

<li>validates outputs
</ul>
<i>It acts like a manager for the skills.</i>
<li>Tool-
external execution capabilities, examples:
<ul type= "circle">
<li>Shell commands

<li>File read/write

<li>Code execution

<li>DB queries

<li>Fetching web data
</ul>
<i>Tools let the model change the world, so they have risk (accidental deletes, unsafe code, etc).</i>
<li>User- User sets:
<ul type="circle">
<li>Intent

<li>Constraints

<li>Examples

<li>Acceptance criteria

<li>Feedback
</ul>
<i>System must stay aligned with user intent.</i>