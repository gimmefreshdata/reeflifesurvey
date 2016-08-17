node {
    stage 'configure'
        def archiveUrl = 'http://reeflifesurvey.com/reef-life-survey/survey-data/dwca.zip'

    stage 'import'
        sh "wget --quiet https://raw.githubusercontent.com/gimmefreshdata/archive-importer/master/archives.groovy -O archives.groovy"
        archives = load 'archives.groovy'
        archives.importIfChanged(archiveUrl)
}
