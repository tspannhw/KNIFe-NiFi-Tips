# KNIFe-NiFi-Tips
tips


### Parse CDC

````

[
  {
    "operation": "shift",
    "spec": {
      "op": {
        "u": {
          "#UPDATE": "op",
          "@(2,after)": "data"
        },
        "c|r": {
          "#INSERT": "op",
          "@(2,after)": "data"
        },
        "d": {
          "#DELETE": "op",
          "@(2,before)": "data"
        },
        "*": "&"
      },
      "before": null,
      "after": null,
      "*": "&"
    }
  }
]


````
