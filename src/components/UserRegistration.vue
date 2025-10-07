<template>
  <div class="user-registration">
    <div class="registration-container">

      <div class="header">
        <h2>Registro de Usuario</h2>
        <p>Complete el formulario para registrarse</p>
      </div>

      <form @submit.prevent="submitForm" novalidate>
        <!-- Campo Nombre -->
        <div class="form-group">
          <label for="nombre">Nombre *</label>
          <input
            id="nombre"
            v-model="form.nombre"
            type="text"
            placeholder="Ingrese su nombre"
          />
          <span v-if="errors.nombre" class="error">{{ errors.nombre }}</span>
        </div>

        <!-- Campo Dirección -->
        <div class="form-group">
          <label for="direccion">Dirección *</label>
          <input
            id="direccion"
            v-model="form.direccion"
            type="text"
            placeholder="Ingrese su dirección"
          />
          <span v-if="errors.direccion" class="error">{{ errors.direccion }}</span>
        </div>

        <!-- Campo Edad -->
        <div class="form-group">
          <label for="edad">Edad *</label>
          <input
            id="edad"
            v-model="form.edad"
            type="number"
            placeholder="Ingrese su edad"
          />
          <span v-if="errors.edad" class="error">{{ errors.edad }}</span>
        </div>

        <!-- Botones -->
        <div class="form-actions">
          <button type="submit" class="btn-submit">Registrar</button>
          <button type="button" @click="resetForm" class="btn-reset">Limpiar</button>
        </div>
      </form>

      <!-- Mensaje de éxito -->
      <div v-if="successMessage" class="success">
        {{ successMessage }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'UserRegistration',
  data() {
    return {
      form: {
        nombre: '',
        direccion: '',
        edad: ''
      },
      errors: {
        nombre: '',
        direccion: '',
        edad: ''
      },
      successMessage: ''
    }
  },
  methods: {
    // Validar formulario completo
    validateForm() {
      this.errors = { nombre: '', direccion: '', edad: '' }
      let isValid = true

      // Validar nombre
      if (!this.form.nombre) {
        this.errors.nombre = 'El nombre es requerido'
        isValid = false
      }

      // Validar dirección
      if (!this.form.direccion) {
        this.errors.direccion = 'La dirección es requerida'
        isValid = false
      }

      // Validar edad
      if (!this.form.edad) {
        this.errors.edad = 'La edad es requerida'
        isValid = false
      } else if (this.form.edad < 18) {
        this.errors.edad = 'Debe ser mayor de 18 años'
        isValid = false
      }

      return isValid
    },
    //ejemplo de camhbio

    // Enviar formulario
    submitForm() {
      if (this.validateForm()) {
        this.successMessage = 'Usuario registrado exitosamente'
        console.log('Datos:', this.form)
        this.resetForm()
        
        setTimeout(() => {
          this.successMessage = ''
        }, 3000)
      }
    },

    // Limpiar formulario
    resetForm() {
      this.form = { nombre: '', direccion: '', edad: '' }
      this.errors = { nombre: '', direccion: '', edad: '' }
    }
  }
}
</script>

<style scoped>
.user-registration {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  padding: 20px;
}

.registration-container {
  background: white;
  border-radius: 15px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
  padding: 30px;
  max-width: 400px;
  width: 100%;
}

.header {
  text-align: center;
  margin-bottom: 30px;
}

.header h2 {
  color: #333;
  margin: 0 0 10px 0;
  font-size: 24px;
}

.header p {
  color: #666;
  margin: 0;
}

.form-group {
  margin-bottom: 20px;
}

label {
  display: block;
  margin-bottom: 5px;
  font-weight: bold;
  color: #333;
}

input {
  width: 100%;
  padding: 12px;
  border: 2px solid #ddd;
  border-radius: 8px;
  font-size: 16px;
  box-sizing: border-box;
}

input:focus {
  outline: none;
  border-color: #667eea;
}

.error {
  color: #e74c3c;
  font-size: 14px;
  margin-top: 5px;
  display: block;
}

.form-actions {
  display: flex;
  gap: 10px;
  margin-top: 25px;
}

.btn-submit, .btn-reset {
  flex: 1;
  padding: 12px;
  border: none;
  border-radius: 8px;
  font-size: 16px;
  cursor: pointer;
  font-weight: bold;
}

.btn-submit {
  background: #27ae60;
  color: white;
}

.btn-submit:hover {
  background: #219a52;
}

.btn-reset {
  background: #95a5a6;
  color: white;
}

.btn-reset:hover {
  background: #7f8c8d;
}

.success {
  background: #d4edda;
  color: #155724;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
  text-align: center;
  border: 1px solid #c3e6cb;
}

/* Responsive */
@media (max-width: 600px) {
  .form-actions {
    flex-direction: column;
  }
}
</style>