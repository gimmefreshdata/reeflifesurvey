node {
    stage 'configure'
        def archiveUrl = 'https://www.dropbox.com/s/swughde1mmgcqnb/reeflifesurvey.zip?dl=1'

    stage 'import'
        sh "wget --quiet https://raw.githubusercontent.com/gimmefreshdata/archive-importer/master/archives.groovy -O archives.groovy"
        archives = load 'archives.groovy'
        archives.importIfChanged(archiveUrl)
}
