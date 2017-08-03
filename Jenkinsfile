@Library('github.com/cloudbeers/multibranch-demo-lib') _

properties([
    parameters([
        booleanParam(
            defaultValue: false,
            description: 'isFoo defaults to false',
            name: 'isFoo'
        )
    ])
])

print 'DEBUG: parameter isFoo = ' + params.isFoo

standardBuild {
    environment = 'golang:1.5.0'
    mainScript = '''
go version
go build -v hello-world.go
'''
    postScript = '''
ls -l
./hello-world
'''
}
