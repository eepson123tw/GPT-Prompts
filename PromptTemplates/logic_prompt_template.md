# 设计一个复杂且嵌套、互相调用且能自我理解的结构

自然语言描述（如 Scenario, Role, Background）提供了一个框架和上下文。
编程结构（如 Define Function, Inputs, Process, Outputs）为模型提供了具体的逻辑流程。
逻辑控制语句（如 If, ElseIf, Else）被用来根据不同条件提出不同的行动方案。
嵌套和递归表现在定义的功能（Function）可以调用其他功能或自身，支持多层逻辑判断和决策。
标记性语言（如 "Inadequate", "Pending", "Lost"）用于标识特定的状态或属性。

```markdown
Scenario: "Planning the Annual Tech Conference"
Role: "Alex, Lead Event Coordinator"
Background: {
  Description: "Alex must organize a tech conference that showcases the latest in tech innovations. 
                The event includes keynotes, panels, and interactive workshops. 
                Alex's tasks include scheduling, logistics, and content curation."
  Context: [
    "Budget constraints are tight due to unexpected costs.",
    "The keynote speaker has not yet confirmed their availability.",
    "A major sponsor just backed out."
  ]
}

Define Function: EvaluateScenario {
  Inputs: {
    "budget_status",
    "keynote_speaker_confirmation",
    "sponsorship_status"
  }
  Process: {
    If "budget_status" is "Inadequate" {
      Suggest Action: "Revise the event budget and cut non-essential costs.";
      Alternative: {
        Query: "Can we increase the budget through other means?";
        If "Yes" {
          Suggest Action: "Approach other potential sponsors immediately.";
        }
        If "No" {
          Suggest Action: "Scale down the event scope to fit the budget.";
        }
      }
    }
    ElseIf "keynote_speaker_confirmation" is "Pending" {
      Suggest Action: "Have a backup speaker on standby.";
      Reminder: {
        Message: "Confirm with the speaker within the next 48 hours.";
      }
    }
    ElseIf "sponsorship_status" is "Lost" {
      Suggest Action: "Ramp up marketing efforts to attract new sponsors.";
      SubProcess: {
        Strategy: "Leverage social media to showcase event benefits.";
        Plan B: {
          Proposal: "Offer additional perks to existing sponsors for increased support.";
        }
      }
    }
  }
  Outputs: {
    "Revised plan based on conditional evaluations.",
    "List of potential sponsors to approach.",
    "Backup speaker details."
  }
}

Invoke Function: EvaluateScenario {
  Arguments: {
    "budget_status": "Inadequate",
    "keynote_speaker_confirmation": "Pending",
    "sponsorship_status": "Lost"
  }
}

End of Scenario
```
