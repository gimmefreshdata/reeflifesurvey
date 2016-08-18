node {
    stage 'configure'
        def archiveUrl = 'https://www.dropbox.com/s/lzy0x7m5v3j21if/reeflifesurvey.textClipping?dl=1'

    stage 'import'
        sh "wget --quiet https://raw.githubusercontent.com/gimmefreshdata/archive-importer/master/archives.groovy -O archives.groovy"
        archives = load 'archives.groovy'
        archives.importIfChanged(archiveUrl)
}
