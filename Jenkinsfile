node('staticsite') {
    git 'https://github.com/Frontarolli/simple-test.git'
    
    stash name: 'website',
      excludes: './trash/**',
      includes: '**'
}

node('linux') {
    unstash 'website'
    sh label: '', script: 'cp index.html /var/www/html/'
}