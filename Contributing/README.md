# Contributing

Contributing refers to the code for storing the history of helps in a manner in which they can be orchestrated by a jitter into an output which meets the intent of that jitter.

# Location

For this example, I've put helps under ![helps](./helps)

# Format

Each help is in a separate folder.  For each help there are two files:

- History.md - a record of who created the help, and which helps directly contributed to this help's creation.  It includes symlinks, author, date and details of how it was generated.
- help.md - the content of the help itself.

# Example

## History.md

'''
    # Genesis Data

    ## Meta Data

    - Type: Help 
    - Author: Eigen November
    - Date: Mon 2024-04-08
    - Model: ChatGPT v4 Turbo
    - Parent: <References any other help that was considered in the production of this help>
    - Merge: <References two previous helps of which this help is a product of their merge >
    - Reference for this help: ./help_name <a universal reference to identify this help>

    ## Intent

    <The context around which this help came into being.  E.g. if it references a stuck, the reference to that stuck is recorded here.  If it is a novel help, what is it trying to acheive.>

    ## Function

    <The advertised function that's used to decide whether this help is of any use.>

    ## Example Result

    <An indication of what result format to expect>

'''

## help.md

    <The 'payload' of the help, varying from a prompt, backed code, text, calls to external APIs and so forth.>