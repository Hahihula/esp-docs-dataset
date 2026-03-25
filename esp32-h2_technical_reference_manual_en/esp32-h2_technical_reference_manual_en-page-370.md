

```markdown
## 10.3.1 Architecture

Figure 10.3-1 shows the architecture of the Event Task Matrix.

The Event Task Matrix has 50 independent channels. A channel can choose any event as input, and map the event to any task as output (For configuration procedures, refer to Section 10.3.2 and Section 10.3.3 respectively). Each channel has an individual enable bit (For configuration procedures, refer to Section 10.3.5).

Figure 10.3-2 illustrates the structure of an ETM channel. The `SOC_ETM_CHn_EVT_ID` field configures the MUX (multiplexer) to select one of the events as the input of channeln. The `SOC_ETM_CHn_TASK_ID` field configures the DEMUX (demultiplexer) to map the event selected by channeln to one of the tasks.
```

```markdown
Figure 10.3-1. Event Task Matrix Architecture

Events ────────────────────────────────────────────────────────────────────────────────────────────── ETM ────────────────────────────────────────────────────────────────────────────────────────────── Tasks

channel0 ────► ────► ────►
channel1 ────► ────► ────►
... ─────────► ────► ────►
channel48 ───► ────► ────►
channel49 ───► ────► ────►

SOC_ETM_CHn_EVT_ID SOC_ETM_CHn_TASK_ID

Figure 10.3-2. ETM Channel Architecture
```