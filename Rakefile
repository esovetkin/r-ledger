desc "Build files for packaging"
task :default do
    sh 'Rscript -e "suppressMessages(devtools::document())"'
    sh 'sudo Rscript -e "devtools::install(quiet=TRUE, upgrade_dependencies=FALSE)"'
    sh "pandoc -o README.md README.rst"
    sh "bean-report inst/extdata/example.beancount ledger > inst/extdata/example.ledger"
    sh "bean-report inst/extdata/example.beancount hledger > inst/extdata/example.hledger"
end

