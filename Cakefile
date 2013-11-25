{exec} = require 'child_process'

task 'test', 'Run unit tests', ->
  exec 'node_modules/mocha/bin/mocha
      --compilers coffee:coffee-script
      --require coffee-script
      --require test/test_helper
      --reporter spec
      --colors', (err, stdout, stderr) ->
    throw err if err
    console.log stdout + stderr

task 'build', 'Convert src/**/*.coffee to lib/**/*.js', ->
  exec 'coffee
      --compile
      --output lib/
      src/', (err, stdout, stderr) ->
    throw err if err
    console.log stdout + stderr
