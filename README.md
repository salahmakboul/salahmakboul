# Salah Eddine Makboul

Software engineering student in Morocco. I study what AI agents do when a process dies in the middle of a task, and I build small fixes that can be tested.

## The question

An agent sends a payment, then gets killed before it saves that fact. What happens when it restarts?

Often it does the action again. An approval has a similar gap: a person says yes to one call, and a different call can run on that yes. I test these failures by really killing processes and counting what happened.

## Call4Agents

[Call4Agents](https://github.com/salahmakboul/call4agents) is a small Python library I maintain. It sits under an existing agent and records each action before and after it runs.

Try it in one command. The demo kills a small agent at every step and shows which action ran twice:

```
pip install call4agents && call4agents crashtest --demo
```

- **Method:** real process kills, then a restart. The test suite also crashes the recovery itself, and old bugs are put back in to check that the tests fail.
- **Runs on:** Python 3.10 to 3.13 on Linux, macOS and Windows, with no required dependencies.
- **Works with:** LangGraph, Pydantic AI, the OpenAI Agents SDK, MCP and plain Python.
- **Limits:** version 0.6 is early, and it has had no independent security audit. If a process dies during an outside call, nobody can tell whether the call went through, so the library stops and asks instead of guessing. An outside tester found real bugs in the approval code, and the [changelog](https://github.com/salahmakboul/call4agents/blob/main/CHANGELOG.md) records them.

[Website](https://salahmakboul.github.io/call4agents/) · [PyPI](https://pypi.org/project/call4agents/) · [Security policy](https://github.com/salahmakboul/call4agents/blob/main/SECURITY.md)

## Other work

- [virtual-A2DP-driver](https://github.com/salahmakboul/virtual-A2DP-driver): a user-mode Bluetooth audio stack for Windows in C++, written from the AVDTP spec. Work in progress.
- [FishoFisho](https://github.com/salahmakboul/FishoFisho-): a real-time Django chat app with an AI assistant and 202 tests. [Live demo](https://fishofisho-sm.onrender.com/).

## Reach me

Open an [issue](https://github.com/salahmakboul/call4agents/issues) or a [discussion](https://github.com/salahmakboul/call4agents/discussions) on Call4Agents, or write to me on [LinkedIn](https://www.linkedin.com/in/salah-eddine-makboul-749927357/). If your agent repeats actions after a crash, I'd like to hear about it and run a crash test on it for free.
