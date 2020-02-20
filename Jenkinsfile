elifePipeline {
    stage 'Checkout', {
        checkout scm
    }

    elifeMainlineOnly {
      stage 'Deploy to staging', {
          sh "helm upgrade --install libero-editor--staging ./helm/libero-editor --recreate-pods"
      }
    }
}