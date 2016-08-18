node {
    stage 'configure'
        def archiveUrl = 'https://github.com/jhammock/reeflifesurvey/archive/master.zip'

    stage 'import'
        sh "wget --quiet https://raw.githubusercontent.com/gimmefreshdata/archive-importer/master/archives.groovy -O archives.groovy"
        archives = load 'archives.groovy'
        archives.importIfChanged(archiveUrl)
}
