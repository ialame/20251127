<script>
import { ref, type Ref } from 'vue'

// Type infere automatiquement
const nombre = ref(0)           // Ref<number>
const texte = ref('hello')      // Ref<string>

  // Type explicite
  const id = ref<string | null>(null)
  const liste = ref<string[]>([])

  // Type complexe
  interface Utilisateur {
  id: number
  nom: string
  email: string
  }

  const utilisateur = ref<Utilisateur | null>(null)

    // Acces type-safe
    utilisateur.value = {
    id: 1,
    nom: 'Alice',
    email: 'alice@example.com'
    }
</script>
