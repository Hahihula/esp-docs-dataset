

```markdown
| State Code | DP Line | DN Line | High-Speed Reception Mode | Corresponding State in Different Modes Control Mode | Escape Mode |
|------------|---------|---------|---------------------------|-----------------------------------------------------|-------------|
| HS-0       | HS Low  | HS High | 0                         | N/A                                                 | N/A         |
| HS-1       | HS High | HS Low  | 1                         | N/A                                                 | N/A         |
| LP-00      | LP Low  | LP Low  | N/A                       | Bridge                                              | Space       |
| LP-01      | LP Low  | LP High | N/A                       | HS-Rqst                                             | 0           |
| LP-10      | LP High | LP Low  | N/A                       | LP-Rqst                                             | 1           |
| LP-11      | LP High | LP High | N/A                       | Stop                                                | N/A         |
```

## 40.5.2 MIPI RX D-PHY Operation

Figure 40.5-2 illustrates the various states and modes of the MIPI RX D-PHY during initialization and active state. Detailed descriptions of each states and modes are presented in the following sections.
```