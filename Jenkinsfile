pipeline {
    agent { label 'spark' }
    node {
        stage 'configure'
            def archiveUrl = 'http://editors.eol.org/eol_php_code/applications/content_server/resources/reef_life_survey.zip'

        stage 'import'
            sh "wget --quiet https://raw.githubusercontent.com/gimmefreshdata/archive-importer/master/archives.groovy -O archives.groovy"
            archives = load 'archives.groovy'
            archives.importIfChanged(archiveUrl)
    }
}
