# Module-18-Challenge

For this project, I am utilizing Python and Visual Studio to create a blockchain-based ledger system. The web interface ledger allows banks to transfer money between senders and receivers then verify the data.

---

## Technologies

This project uses Anaconda, Python, Git Bash, Visual Studio, and Github. This project also uses streamlit.

---

## Installation Guide

These are the required libraries and dependencies:

import streamlit as st

from dataclasses import dataclass

from typing import Any, List

import datetime as datetime

import pandas as pd

import hashlib


---

## Usage

* Step 1

I created a new Record data class.

        @dataclass

        class Record:

            sender: str

            receiver: str

            amount: float


* Step 2

I modified the existing data class to store data from the Record data class.

        @dataclass

        class Block:

            record: Record

            creator_id: int

            prev_hash: str = "0"

            timestamp: str = datetime.datetime.utcnow().strftime("%H:%M:%S")

            nonce: int = 0
    

* Step 3

I added input areas for the user interface then updated the new block.

        sender = st.text_input("Sender Name")

        receiver = st.text_input("Receiver Name")

        amount = st.text_input("Amount")


        new_block = Block(creator_id=42, prev_hash=prev_block_hash, record=Record(sender, receiver, amount))


* Screenshots

Web Interface:

![Initial Web Interface](https://github.com/abcarmin/Module-18-Challenge/blob/main/Screenshot%201.png)


After adding new blocks:

![New Blocks Added](https://github.com/abcarmin/Module-18-Challenge/blob/main/Screenshot%203.png)


After several blocks were added and I validated the chain:

![Validated Chain](https://github.com/abcarmin/Module-18-Challenge/blob/main/Screenshot%205.png)




---

## Contributors

Allyssa Carmin

---

## License

SMU Fintech Course