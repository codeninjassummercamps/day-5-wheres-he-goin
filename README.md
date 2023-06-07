# Day 5 Where's He Goin'?

```template
function walkForward () {
    agent.move(BACK, 3)
}
function evasiveManeuvers () {
    agent.move(FORWARD, 1)
    agent.move(RIGHT, 2)
    agent.move(FORWARD, 2)
    agent.move(LEFT, 3)
}
function lookForward () {
    agent.teleport(agent.getPosition(), NORTH)
}
player.onChat("go", function () {
    goToStart()
    chargeForward()
    leftLoop()
    lookForward()
    chargeForward()
    agent.move(FORWARD, 1)
    rightFork()
    agent.turn(LEFT_TURN)
    agent.turn(LEFT_TURN)
    chargeForward()
    chargeForward()
    chargeForward()
    agent.turn(RIGHT_TURN)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 3)
    lookForward()
    rightFork()
    evasiveManeuvers()
    loops.pause(3000)
    chargeForward()
    agent.move(FORWARD, 1)
    lookForward()
    loops.pause(500)
    walkForward()
})
function goToStart () {
    agent.teleport(world(0, 0, -2), NORTH)
}
function rightFork () {
    agent.turn(RIGHT_TURN)
    chargeForward()
    chargeForward()
}
function chargeForward () {
    for (let index = 0; index < 4; index++) {
        agent.turn(LEFT_TURN)
    }
    agent.move(FORWARD, 3)
}
function leftLoop () {
    agent.turn(LEFT_TURN)
    agent.move(FORWARD, 3)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 4)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 3)
}

```

## Where's He Goin'?

Learn about functions and algorithms by trying to figure out where the agent will go when you use the chat command "go". This is your final Concept Challenge, so it's a bit tricky, but you've got this, ninja!

## What's a Function?

A function is a way to pull out code from your main code. They are helpful for many reasons, like making your code more easy to read, and letting you repeat groups of lines of code. Usually, functions are used for code that will be repeated and code that works together to accomplish one bigger task. However, sometimes functions can be sneaky!


## Step 1 

The main code here is the "go" chat command, but inside of this code there are a LOT of function calls. Read through the code, and try to figure out where the agent will go! Watch out for sneaky functions and code that doesn't do exactly what you'd expect!

## Activity Complete!

Great job! You learned about functions and algorithms!
